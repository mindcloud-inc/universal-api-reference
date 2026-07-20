# Create Campaign with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Campaign](https://docs.vouchery.io/reference/postapiv21campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Campaign type. Use MainCampaign or SubCampaign. |
| `name` | body | `string` | yes | Campaign name. |
| `currency` | body | `string` | yes | Campaign currency code. |
| `status` | body | `string` | no | Campaign status. |
| `description` | body | `string` | no | Campaign description. |
| `team` | body | `string` | no | Campaign team. |
| `template` | body | `string` | no | Campaign template. |
