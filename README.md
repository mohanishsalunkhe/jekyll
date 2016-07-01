# dockyll-s3
Jekyll and s3_website in a Docker container.

README IS INCOMPLETE

docker run --rm -v "$PWD:/src" woodlandh/dockyll-s3 jekyll build

docker run -d -v "$PWD:/src" -p 4000:4000 woodlandh/dockyll-s3 serve -H 0.0.0.0

docker run --rm -v "$PWD:/src" -e "AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID" -e AWS_SECRET_ACCESS_KEY="$AWS_SECRET_ACCESS_KEY" woodlandh/dockyll-s3 s3_website push --dry-run
