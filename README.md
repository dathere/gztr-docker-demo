# gztr-docker-demo

**This setup is NOT intended for production usage.** Rather it is for demonstrative purposes so that you can try ckanext-gztr on your local device.

This is a demo repository for trying out the [ckanext-gztr](https://gztr.dathere.com) CKAN extension on your local device.

This setup is based on [ckan/ckan-docker](https://github.com/ckan/ckan-docker) with modifications.

## Get started locally

Make sure you have Docker and Docker Compose installed on your device. We assume an Ubuntu-like desktop environment for this tutorial and that you are familiar with basic Bash usage.

1. Clone the git repository to your local device.

```bash
git clone https://github.com/dathere/gztr-docker-demo.git
```

2. Copy `.env.example` to `.env` and modify it as needed.

```bash
cd gztr-docker-demo
cp .env.example .env
nano .env # or use a code editor
```

3. Run your local CKAN instance with Docker Compose.

```bash
docker compose -f docker-compose.dev.yml build
docker compose -f docker-compose.dev.yml up
```

4. Explore your CKAN instance at [http://localhost:5000](http://localhost:5000) in your web browser once ran successfully.

5. Follow the relevant installation instructions at [gztr.dathere.com/docs/install](https://gztr.dathere.com/docs/install) for setting up any other necessary configuration such as your STAC catalog and collection files along with GeoParquet data as demonstrated in the Geospatial data section at [gztr.dathere.com/docs/geospatial-data](https://gztr.dathere.com/docs/geospatial-data) where there are notebooks you can view in your browser to learn from.

Hopefully in the future we can add example GeoParquet files that automatically get added to your demo CKAN instance to explore.

If you run into any errors or issues with this setup please [file an issue](https://github.com/dathere/gztr-docker-demo/issues).
