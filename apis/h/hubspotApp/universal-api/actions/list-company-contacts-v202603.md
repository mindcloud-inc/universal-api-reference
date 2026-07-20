# HubSpot: List Company Contacts v2026-03

Retrieves company contacts from HubSpot using the 2026-03 API.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-company-contacts-v202603
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-company-contacts-v202603?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-company-contacts-v202603?${params}`, {
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
| `companyId` | string | yes | The company record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "toObjectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `toObjectId` | string | The associated contact record ID. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/2026-03/objects/companies/:companyId/associations/contacts` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-contacts-v202603.md) for the provider-specific parameters and requirements.

