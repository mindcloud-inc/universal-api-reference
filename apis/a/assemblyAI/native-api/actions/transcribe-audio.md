# Transcribe Audio with AssemblyAI

Creates a new transcript from a media URL in AssemblyAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/transcript`
- **Base URL:** `https://api.assemblyai.com`
- **Official documentation:** [Transcribe Audio](https://www.assemblyai.com/docs/api-reference/transcripts/submit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Publicly reachable audio or video URL to transcribe. |
| `prompt` | body | `string` | no | Contextual prompt text to guide the transcription model. |
| `speech_models[]` | body | `array<string>` | yes | Preferred speech models in priority order. |
| `language_code` | body | `string` | no | Language code for the audio when you want to force a specific language. |
| `language_codes[]` | body | `array<string>` | no | Language codes for code-switching audio. |
| `language_detection` | body | `boolean` | no | Detect the language automatically. |
| `language_detection_options` | body | `object` | no | Options for automatic language detection. |
| `punctuate` | body | `boolean` | no | Add punctuation to the transcript output. |
| `format_text` | body | `boolean` | no | Apply text formatting to the transcript output. |
| `multichannel` | body | `boolean` | no | Enable multichannel transcription for multi-track audio. |
| `speaker_labels` | body | `boolean` | no | Enable speaker diarization. |
| `speaker_options` | body | `object` | no | Options for speaker diarization range handling. |
| `speakers_expected` | body | `number` | no | Expected number of speakers for diarization. |
| `audio_start_from` | body | `number` | no | Start transcribing from this millisecond offset. |
| `audio_end_at` | body | `number` | no | Stop transcribing at this millisecond offset. |
| `auto_highlights` | body | `boolean` | no | Extract key phrases from the transcript. |
| `sentiment_analysis` | body | `boolean` | no | Analyze sentiment across the transcript. |
| `entity_detection` | body | `boolean` | no | Detect entities in the transcript. |
| `content_safety` | body | `boolean` | no | Run content moderation on the transcript. |
| `content_safety_confidence` | body | `number` | no | Confidence threshold for the content safety model. |
| `iab_categories` | body | `boolean` | no | Enable topic detection categories. |
| `redact_pii` | body | `boolean` | no | Redact personally identifiable information in transcript text. |
| `redact_pii_policies[]` | body | `array<string>` | no | PII policy list to enable during redaction. |
| `redact_pii_sub` | body | `string` | no | Replacement logic for detected PII. |
| `redact_pii_audio` | body | `boolean` | no | Generate redacted audio with spoken PII beeped out. |
| `redact_pii_audio_options` | body | `object` | no | Options for PII-redacted audio output. |
| `redact_pii_audio_quality` | body | `string` | no | Output file type for redacted audio. |
| `filter_profanity` | body | `boolean` | no | Filter profanity from transcript text. |
| `remove_audio_tags` | body | `string` | no | Remove audio-event tags from transcript text on supported models. |
| `disfluencies` | body | `boolean` | no | Include filler words like um and uh in the transcript. |
| `custom_spelling[]` | body | `array<object>` | no | Custom spelling and formatting rules using to/from values. |
| `keyterms_prompt[]` | body | `array<string>` | no | Domain-specific words or phrases to improve recognition. |
| `speech_understanding` | body | `object` | no | Speech-understanding tasks such as translation, speaker identification, or custom formatting. |
| `auto_chapters` | body | `boolean` | no | Deprecated auto-chapters toggle. |
| `summarization` | body | `boolean` | no | Deprecated summarization toggle. |
| `summary_model` | body | `string` | no | Deprecated summarization model option. |
| `summary_type` | body | `string` | no | Deprecated summary output type. |
| `webhook_url` | body | `string` | no | Webhook URL to receive transcript completion events. |
| `webhook_auth_header_name` | body | `string` | no | Webhook auth header name for completed or failed webhook deliveries. |
| `webhook_auth_header_value` | body | `string` | no | Webhook auth header value for completed or failed webhook deliveries. |
| `speech_threshold` | body | `number` | no | Minimum fraction of speech required in the audio. |
| `temperature` | body | `number` | no | Control randomness in model output. |
| `language_confidence_threshold` | body | `number` | no | Minimum confidence score required when automatic language detection is enabled. |
