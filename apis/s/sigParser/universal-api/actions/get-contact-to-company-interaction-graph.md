# SigParser: Get Contact-to-Company Interaction Graph



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-contact-to-company-interaction-graph
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-contact-to-company-interaction-graph?connectionId=$CONNECTION_ID&contactEmail=ava%40example.com&relatedCompanyDomain=string&startDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactEmail": "ava@example.com",
  "relatedCompanyDomain": "string",
  "startDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/get-contact-to-company-interaction-graph?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactEmail` | string | yes | Email address of the primary contact. |
| `relatedCompanyDomain` | string | yes | Domain of the related company. |
| `startDate` | date | yes | Start date of the interactions. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigParser API returns.

## Native endpoint

Through the native SigParser API, this operation is `POST /api/Contacts/CompaniesGraph` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-to-company-interaction-graph.md) for the provider-specific parameters and requirements.

