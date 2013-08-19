# S3 Static Mixtape

An experiment in hosting static mixtape websites on S3, with the help of
[cors-bucket-list](https://github.com/zeke/cors-bucket-list), a CORS-friendly
proxy service that dishes up JSON listings of bucket contents.

## Basic Setup

1. Create a [Static Website on S3](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html) and set the index document to `index.html`
1. Upload MP3s to a `songs` directory in your bucket.
1. Set the `bucket` variable in index.html to your bucket name.
1. Upload this repo to your bucket.
1. Ensure all files in your bucket are publicly readable.



curl -H "Origin: http://example.com" --verbose \
  http://s3-mixtape-test.s3.amazonaws.com/songs/lunch.mp3