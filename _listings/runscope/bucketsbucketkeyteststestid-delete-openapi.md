---
swagger: "2.0"
x-collection-name: Runscope
x-complete: 0
info:
  title: Runscope Delete Buckets Tests
  description: Delete a test, including all steps, schedules, test-specific environments
    and results.
  version: 1.0.0
host: api.runscope.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /buckets/{bucketKey}/tests:
    get:
      summary: Get Buckets Tests
      description: Returns a list of tests.
      operationId: buckets.bucketKey.tests.get
      x-api-path-slug: bucketsbucketkeytests-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Buckets
      - Tests
    post:
      summary: Add Buckets Tests
      description: Create a test.
      operationId: buckets.bucketKey.tests.post
      x-api-path-slug: bucketsbucketkeytests-post
      parameters:
      - in: body
        name: NewTest
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Buckets
      - Tests
  /buckets/{bucketKey}/tests/{testId}:
    delete:
      summary: Delete Buckets Tests
      description: Delete a test, including all steps, schedules, test-specific environments
        and results.
      operationId: buckets.bucketKey.tests.testId.delete
      x-api-path-slug: bucketsbucketkeyteststestid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Buckets
      - Tests
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