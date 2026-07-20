# <img src="https://images.mindcloud.co/apps/icons/rev_1773938011065.jpeg" alt="Rev AI logo" width="28" height="28"> Rev AI: Universal API

Rev AI provides speech-to-text transcription and transcript intelligence APIs for prerecorded audio.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/revAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.rev.ai
- **Vendor API docs:** https://docs.rev.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Rev AI. |

### Captions

| Action | Method | Description |
| --- | --- | --- |
| [Get Captions](actions/get-captions.md) | GET | Retrieves captions from Rev AI. |
| [Get Translated Captions](actions/get-translated-captions.md) | GET | Retrieves translated captions from Rev AI. |

### Customvocabulary

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Vocabulary](actions/create-custom-vocabulary.md) | POST | Creates a custom vocabulary in Rev AI. |
| [Delete Custom Vocabulary](actions/delete-custom-vocabulary.md) | DELETE | Deletes a custom vocabulary from Rev AI. |
| [Get Custom Vocabulary](actions/get-custom-vocabulary.md) | GET | Retrieves a custom vocabulary from Rev AI. |
| [List Custom Vocabularies](actions/list-custom-vocabularies.md) | GET | Retrieves custom vocabularies from Rev AI. |

### Sentimentanalysisjob

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sentiment Analysis Job](actions/delete-sentiment-analysis-job.md) | DELETE | Deletes a sentiment analysis job from Rev AI. |
| [Get Sentiment Analysis Job](actions/get-sentiment-analysis-job.md) | GET | Retrieves a sentiment analysis job from Rev AI. |
| [List Sentiment Analysis Jobs](actions/list-sentiment-analysis-jobs.md) | GET | Retrieves sentiment analysis jobs from Rev AI. |
| [Submit Sentiment Analysis Job](actions/submit-sentiment-analysis-job.md) | POST | Creates a sentiment analysis job in Rev AI. |

### Sentimentanalysisresult

| Action | Method | Description |
| --- | --- | --- |
| [Get Sentiment Analysis Result](actions/get-sentiment-analysis-result.md) | GET | Retrieves a sentiment analysis result from Rev AI. |

### Topicextractionjob

| Action | Method | Description |
| --- | --- | --- |
| [Delete Topic Extraction Job](actions/delete-topic-extraction-job.md) | DELETE | Deletes a topic extraction job from Rev AI. |
| [Get Topic Extraction Job](actions/get-topic-extraction-job.md) | GET | Retrieves a topic extraction job from Rev AI. |
| [List Topic Extraction Jobs](actions/list-topic-extraction-jobs.md) | GET | Retrieves topic extraction jobs from Rev AI. |
| [Submit Topic Extraction Job](actions/submit-topic-extraction-job.md) | POST | Creates a topic extraction job in Rev AI. |

### Topicextractionresult

| Action | Method | Description |
| --- | --- | --- |
| [Get Topic Extraction Result](actions/get-topic-extraction-result.md) | GET | Retrieves a topic extraction result from Rev AI. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a transcript from Rev AI. |
| [Get Translated Transcript](actions/get-translated-transcript.md) | GET | Retrieves a translated transcript from Rev AI. |

### Transcriptionjob

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transcription Job](actions/delete-transcription-job.md) | DELETE | Deletes a transcription job from Rev AI. |
| [Get Transcription Job](actions/get-transcription-job.md) | GET | Retrieves a transcription job from Rev AI. |
| [List Transcription Jobs](actions/list-transcription-jobs.md) | GET | Retrieves transcription jobs from Rev AI. |
| [Submit Transcription Job](actions/submit-transcription-job.md) | POST | Creates a new transcription job in Rev AI. |

### Transcriptsummary

| Action | Method | Description |
| --- | --- | --- |
| [Get Transcript Summary](actions/get-transcript-summary.md) | GET | Retrieves a transcript summary from Rev AI. |

