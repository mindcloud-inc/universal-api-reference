# Create Quick Answer with Umbler Talk

Creates a new quick answer in Umbler Talk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/quick-answers/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [Create Quick Answer](https://app-utalk.umbler.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Quick answer content. |
| `name` | body | `string` | yes | Quick answer name. |
| `organizationId` | body | `string` | yes | The organization ID. |
| `visibility` | body | `string` | yes | Quick answer visibility. |
