---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix AppHub ARCS Get the privileges information
  description: Get the privileges information
  termsOfService: Terms of service
  contact:
    name: 'Digital Predix AppHub ARCS: Development'
  version: 1.0.0
host: predix-apphub-arcs-prod.run.aws-usw02-pr.ice.predix.io
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /privileges:
    get:
      summary: Get the privileges information
      description: Get the privileges information
      operationId: getPrivilegeUsingGET
      x-api-path-slug: privileges-get
      responses:
        200:
          description: OK
      tags:
      - Privileges
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---