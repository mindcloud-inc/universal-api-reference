# Test Webhook URL with Transcript Downloader

Tests a webhook URL in Transcript Downloader.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhook/test`
- **Base URL:** `https://dashboard.transcriptdownloader.com`
- **Official documentation:** [Test Webhook URL](https://documentation.transcriptdownloader.com/webhooks#1-test-your-webhook-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webhook URL to test. |
