# Start Service
	systemctl start docker

# Docker
	cd /Docker/App/web2py-gunicorn-nginx
	chmod 775 run.sh
	./run.sh

# Docker Compose
	pip install docker-compose
	cd /Docker/App/web2py-gunicorn-nginx
	docker-compose up -d
	docker-compose ps
	docker network ls
	docker network inspect root_default
	docker volume ls
	docker volume inspect root_applications

# Docker Stack
	docker swarm init --advertise-addr $(hostname -i)
	docker stack deploy -c docker-compose.yml web2py-gunicorn-nginx
	docker stack ls
	docker stack ps web2py-gunicorn-nginx
	docker stack services web2py-gunicorn-nginx

# Shell (Copy the content of the file into this scaffolding shell and replace the variable text $ with \$ )
cat << EOF > docker-compose.yml

EOF
cat docker-compose.yml

cat << EOF > run.sh

EOF
cat run.sh

cat << EOF > w2p.conf

EOF
cat w2p.conf

cat << EOF > web2py-gunicorn

EOF
cat web2py-gunicorn

cat << EOF > web2py-nginx

EOF
cat web2py-nginx

chmod 755 run.sh
./run.sh

docker-compose up -d
docker-compose ps
