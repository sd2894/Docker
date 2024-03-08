Install Magento 2.4.6 on Windows using Docker
------------------------------------------------------

1. Download Docker for Windows - https://lnkd.in/dDpCHGqx
2. Install the Magento 2.4.6 package in the local folder (Ex. E:\magento\magento2) - composer create-project --repository-url=https://repo.magento.com/ magento/project-community-edition=2.4.6 magento2
3. Change memory_limit = 2048M in user.ini file (Ex. E:\magento\magento2\user.ini)
4. Download the docker-compose.yml file at this link - https://lnkd.in/dzmWnfdx
5. Paste the docker-composer.yml file in the location "C:\Program Files\Docker\Docker".
6. Sign up in the docker and Open the cmd prompt in the location [C:\Program Files\Docker\Docker] run CLI step-by-step
      1. docker-compose up -d --build
      2. docker exec -it web bash
      3. ls
      4. cd app
      5. In browser run http://localhost:8080/index.php - create a database in PHPMyAdmin
      6. In cmd prompt - php bin/magento setup: install --base-url="https://lnkd.in/dCvdH_Jy" --base-url-secure="https://lnkd.in/dCvdH_Jy" --db-host="mysql" --db-name="mage246" --db-user="root" --db-password="root" --admin-firstname="admin" --admin-lastname="admin" --admin-email="example@gmail.com" --admin-user="admin" --admin-password="admin123" --language="en_US" --currency="USD" --timezone="America/Chicago" --use-rewrites="1" --backend-frontname="admin" --search-engine=elasticsearch7 --elasticsearch-host="elasticsearch" --elasticsearch-port=9200
      7. php bin/magento s:up 
      8. php bin/magento s:d:c
      9. php bin/magento s:s:d -f
7. In some cases, add an entry to your host's file (C:\Windows\System32\drivers\etc\hosts on Windows).
