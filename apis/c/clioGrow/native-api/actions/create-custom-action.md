# Create Custom Action with Clio Grow

## Endpoint

- **Method:** `POST`
- **Path:** `/custom_actions`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [Create Custom Action](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Custom-Actions/operation/CustomAction%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.label` | body | `string` | yes | The label of the custom action. Maximum length: 32. |
| `data.target_url` | body | `string` | yes | The target HTTPS URL of the custom action. |
| `data.ui_reference` | body | `string` | yes | The UI reference for the custom action. Clio currently supports matters/show. Accepted values: `0`. |
