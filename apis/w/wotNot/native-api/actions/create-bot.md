# Create Bot with WotNot

Creates a new bot in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bot`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Create Bot](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the new bot |
| `template_id` | body | `number` | yes | Reference bot ID to clone from |
