---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Add Column
  description: Add a Column to a DataSet
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /dataset/{dataSetId}/column:
    post:
      summary: Add Column
      description: Add a Column to a DataSet
      operationId: dataSetColumnAdd
      x-api-path-slug: datasetdatasetidcolumn-post
      parameters:
      - in: formData
        name: columnOrder
        description: The display order for this column
      - in: formData
        name: dataSetColumnTypeId
        description: The column type for this column
      - in: path
        name: dataSetId
        description: The DataSet ID
      - in: formData
        name: dataTypeId
        description: The data type ID for this column
      - in: formData
        name: formula
        description: MySQL SELECT syntax formula for this Column if the column type
          is formula
      - in: formData
        name: heading
        description: The heading for the Column
      - in: formData
        name: listContent
        description: A comma separated list of content for drop downs
      - in: formData
        name: remoteField
        description: JSON-String to select Data from the Remote DataSet
      - in: formData
        name: showFilter
        description: Flag indicating whether this column should present a filter on
          DataEntry
      - in: formData
        name: showSort
        description: Flag indicating whether this column should allow sorting on DataEntry
      responses:
        200:
          description: OK
      tags:
      - Column
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