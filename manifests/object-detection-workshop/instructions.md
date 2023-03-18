prep
- Install RHODS, ODF, Pipelines.
- Deploy dspipelines and elyra OBCs.
- Update and deploy Pipelines CR.
- Publish port 3000 in pipelines-ui service.
- Set up build config and imagestream for custom object detection notebook.
- Update and deploy cluster manifest
- Update and deploy user manifest

users
- log into RHODS
- step into project
- create workbench with object detection image
- review obc credentials (secret user-x)
- add data connection with obc credentials, mount into workbench
- log into workbench
- clone od repository
- work on notebooks, browse S3 bucket

- configure model server, create route
- deploy model, note prediction endpoint
- run online scoring

- deploy model client with PREDICTION_URL
- deploy frontend
- test endpoints
- test frontend app
- test app on mobile (QR code)

- run offline scoring notebook
- review results in S3 bucket
- review offline scoring pipeline, rename
- fill in S3 credentials, PVC name
- submit pipeline, review in KFP dashboard
- review results in S3 bucket


S3 endpoint:
http://s3.openshift-storage.svc

model client repo:
https://github.com/mamurak/object-detection-rest.git

env:
PREDICTION_URL

frontend repo:
https://github.com/rh-aiservices-bu/object-detection-app.git

env:
OBJECT_DETECTION_URL = http://object-detection-rest:8080/predictions

model path:
tiny-yolov3-11.onnx

QR code generator:
https://www.qr-code-generator.com/