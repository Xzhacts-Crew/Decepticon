# Pengamanan Server dengan Memanipulasi SSH

# Nama Anggota Kelompok
1. Aditya Farrel Firdaus            : 22.83.0825
3. Muhamad Iqbal Ashari             : 22.83.0818
4. Rayyan Abdie Azzaky              : 22.83.0811
5. Muhammad Priandika Bayu Firdaus  : 22.83.0798
6. Tri Azani                        : 22.83.0764
 
# Service keamanan 
- Cowrie (Manipulasi SSH)
- Web Server
- CloudFlare


# Installasi Cowrie

git clone http://github.com/cowrie/cowrie

cd cowrie

sudo apt-get install python3-virtualenv python3-dev libssl-dev libffi-dev build-essential libpython3-dev libjpeg-dev libpng-dev libfreetype6-dev

python3 -m venv cowrie-env

source cowrie-env/bin/activate

pip install cowrie

cp cowrie.cfg.dist cowrie.cfg


# Langkah Demo
- Cowrie (Manipulasi SSH)


  Tampilan Login Peretas Memasuki SSH
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/e3fe5417-8e65-4f31-a9ad-011aa974f117)

  Tampilan Login dari SSH Server (menggunakan port 2525)
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/51560d61-3766-4c5d-a4ee-05fffdfecad5)


- Uji Coba Cowrie


  Peretas membuat direktori pada SSH palsu
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/f4f2431e-36d2-4d52-813a-4db9a8d9a8c2)
  ketika Peretas membuat direktori, tidak masuk kedalam server
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/dac914b7-b5b8-42a2-b644-008d1b4b7c42)

- Log Cowrie

  
  Tampilan SSH Peretas
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/f6421c9b-328c-40ec-855d-8186157340bb)

  Log Server

  
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/e4f56bf9-d021-4ef3-bca8-3e08fedfad51)
  
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/74691e4e-c9d6-45e5-924a-903664f07cc3)

# Wordpress

- install Wordpress

  wget https://wordpress.org/latest.zip

  unzip latest.zip

  ls | grep wordpress

  sudo mv wordpress/ /var/www/html/

  sudo chown www-data:www-data -R /var/www/html/wordpress/

  sudo chmod -R 755 /var/www/html/wordpress/

  sudo nano /etc/apache2/sites-available/wordpress.conf
  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/e068590b-9043-4785-ae17-ee8b0f394303)

  sudo a2ensite wordpress.conf

  sudo a2enmod rewrite

  sudo systemctl restart apache2
  
  
- Tampilan Wordpress

  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/730c306c-fb1e-4054-9f12-9470e9732d81)

  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/7b00706f-f4b7-405f-931a-a185b84d1295)

  ![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/d4a5753f-d4bc-43c0-8326-b1f0774efa6b)


# Cloudflare

curl -L --output cloudflared.deb https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb && 

sudo dpkg -i cloudflared.deb && 

sudo cloudflared service install eyJhIjoiZTFjODJhNjMwYjRiZDE4NGQ5NGU0ZDdhYWZiYWFkOGYiLCJ0IjoiNGExOGFiY2MtM2EzMy00MTFkLThmYWQtZjBmZWI5MWYyMDMyIiwicyI6Ik1HRTFNRFF6TldJdE5UZzNPUzAwWTJVNUxXRTBObUl0WmpObU4yVTNOalU1TnpNMCJ9

masuk pada bagian public hostname

![image](https://github.com/Xzhacts-Crew/Decepticon/assets/144193006/d72c16be-6366-400f-bae1-7521e8f9ea08)






  
