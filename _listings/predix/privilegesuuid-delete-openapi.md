---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix AppHub ARCS Delete the privileges information
  description: Delete the privileges information
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
    post:
      summary: Save the privileges information
      description: Save the privileges information
      operationId: savePrivilegeUsingPOST
      x-api-path-slug: privileges-post
      parameters:
      - in: body
        name: request
        description: request
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Privileges
  /privileges/{uuid}:
    put:
      summary: Update the privileges information
      description: Update the privileges information
      operationId: updatePrivilegeUsingPUT
      x-api-path-slug: privilegesuuid-put
      parameters:
      - in: body
        name: request
        description: request
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Privileges
      - Uuid
    delete:
      summary: Delete the privileges information
      description: Delete the privileges information
      operationId: deletePrivilegeUsingDELETE
      x-api-path-slug: privilegesuuid-delete
      parameters:
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Privileges
      - Uuid
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