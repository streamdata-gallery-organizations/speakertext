---
swagger: "2.0"
x-collection-name: SpeakerText
x-complete: 1
info:
  title: Speaker Text
  description: speakertexts-transcription-services-may-be-accessed-through-a-restful-api--it-is-possible-to-initiate-transcription-and-receive-transcription-results-through-the-api--anyone-with-a-speakertext-account-can-use-the-api-
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
---