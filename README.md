# bsidescincy.org
BSidesCincy website source

Website is build using the Hexo Framework:
* https://hexo.io/docs/

More or less how build & deployment work:
```bash
# This will run a server on http://localhost:4000/ which can give a local preview of the site:
hexo s

# This builds the static files from the source socuments in ./public/, after cleaning the folders first
hexo clean
hexo gen

# You can deploy the static files to a test S3 bucket that you've created or been granted rights on:
aws s3 sync --delete ./public/ s3://bsidescincy-test/
# Then, visit http://bsidescincy-test.s3-website.<region>.amazonaws.com/ to test it in the wild

# This deploys the static files to the s3 bucket, using the convention common to AWS S3 web hosting:
aws s3 sync --delete ./public/ s3://bsidescincy.org/
```
