# <img src="https://images.mindcloud.co/apps/icons/encodian_1777477355150.jpeg" alt="Encodian - General logo" width="28" height="28"> Encodian - General: Universal API

Encodian Flowr General provides Power Automate-compatible actions for AI document processing, translation, archive creation and extraction, email processing, file search/replace, and subscription status checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianGeneral/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr/
- **Vendor API docs:** https://learn.microsoft.com/en-us/connectors/encodiangeneral/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Subscription Flowr And Vertr Status](actions/subscription-flowr-and-vertr-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Email Extract Attachments](actions/email-extract-attachments.md) | GET | Extracts attachments from an email file in Encodian. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [AI Process Bank Check US](actions/ai-process-bank-check-us.md) | GET | Extracts US bank check data with Encodian AI. |
| [AI Process Bank Statement US](actions/ai-process-bank-statement-us.md) | GET | Extracts US bank statement data with Encodian AI. |
| [AI Process Contract](actions/ai-process-contract.md) | GET | Extracts contract data from a file with Encodian AI. |
| [AI Process Credit Card](actions/ai-process-credit-card.md) | GET | Extracts credit card data from images with Encodian AI. |
| [AI Process Health Insurance Card US](actions/ai-process-health-insurance-card-us.md) | GET | Extracts US health insurance card data with Encodian AI. |
| [AI Process ID Document](actions/ai-process-id-document.md) | GET | Extracts ID document data from a file with Encodian AI. |
| [AI Process Invoice](actions/ai-process-invoice.md) | GET | Extracts invoice data from a file with Encodian AI. |
| [AI Process Mortgage Document US](actions/ai-process-mortgage-document-us.md) | GET | Extracts US mortgage document data with Encodian AI. |
| [AI Process Pay Stub US](actions/ai-process-pay-stub-us.md) | GET | Extracts US pay stub data with Encodian AI. |
| [AI Process Receipt](actions/ai-process-receipt.md) | GET | Extracts receipt data from a file with Encodian AI. |
| [AI Process Tax Document US](actions/ai-process-tax-document-us.md) | GET | Extracts US tax document data with Encodian AI. |
| [AI Speech To Text](actions/ai-speech-to-text.md) | GET | Transcribes speech from an audio file in Encodian. |
| [AI Translate File](actions/ai-translate-file.md) | POST | Translates a file to a target language with Encodian AI. |
| [File Replace Text With Image](actions/file-replace-text-with-image.md) | PUT | Replaces text placeholders with images in a file. |
| [File Search And Replace Text](actions/file-search-and-replace-text.md) | PUT | Searches and replaces text in a file. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Email Extract Metadata](actions/email-extract-metadata.md) | GET | Extracts metadata from an email file in Encodian. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Archive Create ZIP](actions/archive-create-zip.md) | POST | Creates a ZIP archive from files in Encodian. |
| [Archive Extract](actions/archive-extract.md) | GET | Extracts files from a ZIP archive in Encodian. |
| [Archive Extract V2](actions/archive-extract-v2.md) | GET | Extracts files from a ZIP archive with Encodian V2. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [AI Run Prompt Text](actions/ai-run-prompt-text.md) | POST | Runs a custom AI text prompt in Encodian. |
| [AI Translate Text Multiple](actions/ai-translate-text-multiple.md) | POST | Translates multiple text strings with Encodian AI. |
| [AI Translate Text Single](actions/ai-translate-text-single.md) | POST | Translates a text block with Encodian AI. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Subscription Flowr And Vertr Status](actions/subscription-flowr-and-vertr-status.md) | GET | Retrieves Flowr and Vertr subscription status from Encodian. |

