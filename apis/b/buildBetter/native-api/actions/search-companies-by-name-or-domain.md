# Search Companies By Name Or Domain with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [Search Companies By Name Or Domain](https://docs.buildbetter.ai/pages/CRM%20Integration/companies#company-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchText` | body | `string` | yes | Find companies whose name or domain matches this text. |
| `limit` | body | `number` | no | Maximum number of companies to return. |
