# BSides Cincy Website - bsidescincy.org

All source for the BSides Cincy website.

Website is build using the Hugo Framework:
* https://gohugo.io/

## Getting Started

```bash
git submodule init
git submodule update
```

## Development

To develop this website, yo must have the `hugo` CLI installed. Once you do, you can serve the development server using:

```bash
hugo server -D
```

### Hero Picture

Dimensions / Aspect Ratio: `1922 × 1080`

### Blog Pictures

`image` Dimensions / Aspect Ratio: `4 x 5`
`feature_image` Dimensions / Aspect Ratio: `16 x 9`

### CSS Override

The CSS override for the theme is located at `css/override.css`

## Deploymenent

```bash
# You can deploy the static files to a test S3 bucket that you've created or been granted rights on:
aws s3 sync --delete ./public/ s3://bsidescincy-test/
# Then, visit http://bsidescincy-test.s3-website.<region>.amazonaws.com/ to test it in the wild

# This deploys the static files to the s3 bucket, using the convention common to AWS S3 web hosting:
aws s3 sync --delete ./public/ s3://bsidescincy.org/
```
