---
swagger: "2.0"
x-collection-name: SpeakerText
x-complete: 0
info:
  title: Speaker Text Retrieve Transcription
  description: This method is used to retrieve the results of SpeakerText transcriptions.
  termsOfService: http://speakertext.com/tos
  version: v1
host: api.speakertext.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /transcripts:
    post:
      summary: Iniate Transcript
      description: This method is used to initiate one or more SpeakerText transcriptions.
      operationId: postTranscripts
      x-api-path-slug: transcripts-post
      parameters:
      - in: query
        name: pingback_url
        description: If present, we will make a POST request to this URL upon transcript
          completion
      - in: query
        name: sources
        description: (JSON) single source object or array of source objects
      responses:
        200:
          description: OK
      tags:
      - Transcripts
  /transcripts/{id}:
    get:
      summary: Retrieve Transcription
      description: This method is used to retrieve the results of SpeakerText transcriptions.
      operationId: getTranscripts
      x-api-path-slug: transcriptsid-get
      parameters:
      - in: query
        name: format
        description: dfxp, srt, txt, xml, or html (for CaptionBox)
      - in: query
        name: id
        description: Transcript ID returned to you upon transcript creation
      responses:
        200:
          description: OK
      tags:
      - Transcripts
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