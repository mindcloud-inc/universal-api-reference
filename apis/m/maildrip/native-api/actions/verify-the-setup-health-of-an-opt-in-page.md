# Verify the setup health of an opt-in page with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/opt-in-pages/{pageId}/verify-setup`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Verify the setup health of an opt-in page](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `string` | yes | ID of the opt-in page to verify |
