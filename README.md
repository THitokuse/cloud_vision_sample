# Google Cloud Vision Sample

## Google Cloud Ruby Github
https://github.com/googleapis/google-cloud-ruby/blob/master/README.md#cloud-vision-api-alpha

**Quick Start**

```
$ gem install google-cloud-vision
```

**Preview**

```
require "google/cloud/vision"

image_annotator_client = Google::Cloud::Vision::ImageAnnotator.new
gcs_image_uri = "gs://gapic-toolkit/President_Barack_Obama.jpg"
source = { gcs_image_uri: gcs_image_uri }
image = { source: source }
type = :FACE_DETECTION
features_element = { type: type }
features = [features_element]
requests_element = { image: image, features: features }
requests = [requests_element]
response = image_annotator_client.batch_annotate_images(requests)
```
