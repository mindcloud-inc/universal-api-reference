# Scribeless: Create Recipients



```
POST https://connect.mindcloud.co/v1/universal/scribeless/latest/actions/create-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scribeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scribeless/latest/actions/create-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scribeless/latest/actions/create-recipients', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The Scribeless campaign ID that will receive the recipients. |
| `data[]` | array<object> | yes | Array of recipient payload objects for multiple Scribeless recipients. |
| `data[].title` | string | no | Recipient title such as Mr or Mrs. |
| `data[].firstName` | string | no | Recipient first name. |
| `data[].lastName` | string | no | Recipient last name. |
| `data[].company` | string | no | Recipient company name. |
| `data[].address` | object | no | Recipient mailing address object. |
| `data[].address.address1` | string | no | First line of the mailing address. |
| `data[].address.address2` | string | no | Second line of the mailing address. |
| `data[].address.address3` | string | no | Third line of the mailing address. |
| `data[].address.city` | string | no | City for the mailing address. |
| `data[].address.state` | string | no | State, county, or region for the mailing address. |
| `data[].address.postalCode` | string | no | Postal or ZIP code for the mailing address. |
| `data[].address.country` | string | no | Two-letter country code for the mailing address. |
| `data[].variables` | object | no | Custom variable values for Scribeless merge fields. |
| `data[].variables.custom1` | string | no | Value for the custom1 merge field. |
| `data[].variables.custom2` | string | no | Value for the custom2 merge field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scribeless API returns.

## Native endpoint

Through the native Scribeless API, this operation is `POST /api/recipients` (base URL `https://platform.scribeless.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipients.md) for the provider-specific parameters and requirements.

