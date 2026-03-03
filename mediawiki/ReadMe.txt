🚀 How to Run

Create a folder:

mkdir mediawiki-docker
cd mediawiki-docker

Save the above file as:

docker-compose.yml

Start containers:

docker compose up -d

Open in browser:

http://localhost:8080

Complete MediaWiki installation from browser.

🔑 Database Details (During Setup)

Use these values in installer:

Field	Value
Database type	MySQL
Database host	db
Database name	mediawiki
Database user	wikiuser
Database password	wikipassword
📁 After Installation (Important)

After setup finishes:

Download LocalSettings.php

Place it inside the running container:

docker cp LocalSettings.php mediawiki_app:/var/www/html/
docker restart mediawiki_app
🛑 Stop Containers
docker compose down