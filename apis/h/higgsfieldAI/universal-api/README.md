# <img src="https://images.mindcloud.co/apps/icons/higgsfield-ai_1776104343644.png" alt="Higgsfield AI logo" width="28" height="28"> Higgsfield AI: Universal API

Generate and manage AI images and videos with Higgsfield's unified model API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/higgsfieldAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloud.higgsfield.ai
- **Vendor API docs:** https://docs.higgsfield.ai/how-to/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Request Status](actions/get-request-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higgsfieldAI/latest/actions/get-request-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Generate File Upload URL](actions/generate-file-upload-url.md) | POST |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Pending Request](actions/cancel-pending-request.md) | PUT | Cancels a pending generation request in Higgsfield AI. |
| [Generate Image with Seedream v4](actions/generate-image-with-seedream-v4.md) | POST |  |
| [Generate Image with Soul Standard](actions/generate-image-with-soul-standard.md) | POST | Creates an image with Soul Standard in Higgsfield AI. |
| [Generate Video with DoP Standard](actions/generate-video-with-dop-standard.md) | POST | Creates a video with DoP Standard in Higgsfield AI. |
| [Generate Video with Kling 2.1 Pro](actions/generate-video-with-kling21-pro.md) | POST | Creates a video with Kling 2.1 Pro in Higgsfield AI. |
| [Generate Video with Seedance 1.0 Pro](actions/generate-video-with-seedance10-pro.md) | POST | Creates a video with Seedance 1.0 Pro in Higgsfield AI. |
| [Get Request Status](actions/get-request-status.md) | GET | Retrieves a generation request status from Higgsfield AI. |
| [Submit Generation Request](actions/submit-generation-request.md) | POST | Submits a generation request to Higgsfield AI. |

