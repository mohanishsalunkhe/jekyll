[![](https://images.microbadger.com/badges/image/woodlandh/dockyll-s3.svg)](https://microbadger.com/images/woodlandh/dockyll-s3 "Get your own image badge on microbadger.com")

# dockyll-s3
Jekyll and s3_website in a Docker container.

###WARNING

Large Docker image size. I've made no attempt (yet) to minimize it. Sorry! Didn't see an easy ruby+java win. Maaaaybe it should be two containers... whoops.

###Versions

* Jekyll 2.5.3
* s3_website 2.12.1

###Examples

Run in your Jekyll root directory, including your \_config.yml file, and your s3_website.yml file.

	docker run --rm -v "$PWD:/src" woodlandh/dockyll-s3 jekyll build

	docker run -d -v "$PWD:/src" -p 4000:4000 woodlandh/dockyll-s3 jekyll serve -H 0.0.0.0

	docker run --rm -v "$PWD:/src" -e "AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID" -e AWS_SECRET_ACCESS_KEY="$AWS_SECRET_ACCESS_KEY" woodlandh/dockyll-s3 s3_website push --dry-run

I'll write this up properly another time.
