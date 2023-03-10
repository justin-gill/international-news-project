# International News Project
##### A very real news site built with Django and React

---

View the live site [here!](https://internationalnewsproject.com)

### About this Project
International News Project is a satirical news site where most of the article content and images are created by OpenAI's GPT-3 and DALL·E, respectively. The article titles are not generated by OpenAI. 


### Running
* [Install docker-compose](https://docs.docker.com/compose/install/#install-compose)
* Fill `.env` for both frontend and backend
* Development
    * `docker-compose -f docker-compose-dev.yaml up`
* Prod
    * `docker-compose build`
    * `./init-letsencrypt.sh` from [nginx-certbot](https://github.com/wmnnd/nginx-certbot) for SSL
    * `docker-compose up`
* Access django shell with 
    * ```docker exec -it $(docker ps -aqf "name=international-news-project-backend") python backend/manage.py```
---

## Hosting
* Currently hosted using GCP Compute Engine, Cloud SQL for PostgreSQL, and a Cloud Storage Bucket for static images. A little overkill for such a simple app, but it works!