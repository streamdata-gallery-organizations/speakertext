{
  "info": {
    "name": "Speaker Text Iniate Transcript",
    "_postman_id": "2c42e5e5-30ea-4e71-9ba1-a67eae011c2c",
    "description": "This method is used to initiate one or more SpeakerText transcriptions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transcripts",
      "item": [
        {
          "id": "8fd13010-fe90-470e-aae5-34f33624f4fe",
          "name": "postTranscripts",
          "request": {
            "url": "http://api.speakertext.com/v1/transcripts?pingback_url=%7B%7D&sources=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "This method is used to initiate one or more SpeakerText transcriptions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0a0efe73-ec8f-48d3-97e1-bb594c498600"
            }
          ]
        }
      ]
    }
  ]
}