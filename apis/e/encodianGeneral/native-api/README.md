# Encodian - General: Native API Reference

A consolidated summary of Encodian - General's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/encodiangeneral/
- **API base URL:** `https://api.apps-encodian.com`

## Authentication

### API Key

Encodian Flowr General uses API key authentication. The Microsoft connector reference lists API Key as required and Region as optional; MindCloud sends the API key using the X-ApiKey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://learn.microsoft.com/en-us/connectors/encodiangeneral/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [AI Process Bank Check US](actions/ai-process-bank-check-us.md) | `POST /api/v1/General/AIProcessBankCheckUS` | [docs](https://support.encodian.com/hc/en-gb/articles/19806562595484) |
| [AI Process Bank Statement US](actions/ai-process-bank-statement-us.md) | `POST /api/v1/General/AIProcessBankStatementUS` | [docs](https://support.encodian.com/hc/en-gb/articles/19807728511516) |
| [AI Process Contract](actions/ai-process-contract.md) | `POST /api/v1/General/AIProcessContract` | [docs](https://support.encodian.com/hc/en-gb/articles/18583890798620) |
| [AI Process Credit Card](actions/ai-process-credit-card.md) | `POST /api/v1/General/AIProcessCreditCard` | [docs](https://support.encodian.com/hc/en-gb/articles/19807871170460) |
| [AI Process Health Insurance Card US](actions/ai-process-health-insurance-card-us.md) | `POST /api/v1/General/AIProcessHealthInsuranceCardUS` | [docs](https://support.encodian.com/hc/en-gb/articles/18584148204956) |
| [AI Process ID Document](actions/ai-process-id-document.md) | `POST /api/v1/General/AIProcessIDDocument` | [docs](https://support.encodian.com/hc/en-gb/articles/18583935825308) |
| [AI Process Invoice](actions/ai-process-invoice.md) | `POST /api/v1/General/AIProcessInvoice` | [docs](https://support.encodian.com/hc/en-gb/articles/18583998185116) |
| [AI Process Mortgage Document US](actions/ai-process-mortgage-document-us.md) | `POST /api/v1/General/AIProcessMortgageUS` | [docs](https://support.encodian.com/hc/en-gb/articles/19808100431004) |
| [AI Process Pay Stub US](actions/ai-process-pay-stub-us.md) | `POST /api/v1/General/AIProcessPayStubUS` | [docs](https://support.encodian.com/hc/en-gb/articles/19808015461916) |
| [AI Process Receipt](actions/ai-process-receipt.md) | `POST /api/v1/General/AIProcessReceipt` | [docs](https://support.encodian.com/hc/en-gb/articles/18584183726876) |
| [AI Process Tax Document US](actions/ai-process-tax-document-us.md) | `POST /api/v1/General/AIProcessTaxUS` | [docs](https://support.encodian.com/hc/en-gb/articles/19808162127644) |
| [AI Run Prompt Text](actions/ai-run-prompt-text.md) | `POST /api/v1/General/AIRunPromptText` | [docs](https://support.encodian.com/hc/en-gb/articles/19106024843932) |
| [AI Speech To Text](actions/ai-speech-to-text.md) | `POST /api/v1/General/AISpeechToText` | [docs](https://support.encodian.com/hc/en-gb/articles/15851898717340) |
| [AI Translate File](actions/ai-translate-file.md) | `POST /api/v1/General/AITranslateFile` | [docs](https://support.encodian.com/hc/en-gb/articles/13790274285724) |
| [AI Translate Text Multiple](actions/ai-translate-text-multiple.md) | `POST /api/v1/General/AITranslateTextMultiple` | [docs](https://support.encodian.com/hc/en-gb/articles/13670267593628) |
| [AI Translate Text Single](actions/ai-translate-text-single.md) | `POST /api/v1/General/AITranslateText` | [docs](https://support.encodian.com/hc/en-gb/articles/13568846675996) |
| [Archive Create ZIP](actions/archive-create-zip.md) | `POST /api/v1/General/AddToZip` | [docs](https://support.encodian.com/hc/en-gb/articles/360002674918-Add-to-Archive-ZIP) |
| [Archive Extract](actions/archive-extract.md) | `POST /api/v1/General/ExtractFromArchive` | [docs](https://support.encodian.com/hc/en-gb/articles/11853992723484) |
| [Archive Extract V2](actions/archive-extract-v2.md) | `POST /api/v1/General/ExtractFromArchiveV2` | [docs](https://support.encodian.com/hc/en-gb/articles/21005901841564) |
| [Email Extract Attachments](actions/email-extract-attachments.md) | `POST /api/v1/General/GetEmailAttachments` | [docs](https://support.encodian.com/hc/en-gb/articles/10531671561629) |
| [Email Extract Metadata](actions/email-extract-metadata.md) | `POST /api/v1/General/GetEmailInfo` | [docs](https://support.encodian.com/hc/en-gb/articles/12237799140252) |
| [File Replace Text With Image](actions/file-replace-text-with-image.md) | `POST /api/v1/General/SearchAndReplaceTextWithImage` | [docs](https://support.encodian.com/hc/en-gb/articles/360027234874) |
| [File Search And Replace Text](actions/file-search-and-replace-text.md) | `POST /api/v1/General/SearchAndReplaceText` | [docs](https://support.encodian.com/hc/en-gb/articles/360020937853-Search-and-Replace-Text) |
| [Subscription Flowr And Vertr Status](actions/subscription-flowr-and-vertr-status.md) | `GET /api/v1/General/GetSubscriptionStatus` | [docs](https://support.encodian.com/hc/en-gb/articles/360010176717-Get-Subscription-Status) |
