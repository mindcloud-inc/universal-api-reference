# Referral Rock: Get Program

Retrieves a referral program from Referral Rock by name.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-program?connectionId=$CONNECTION_ID&programName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "programName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/get-program?${params}`, {
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
| `programName` | string | yes | The name of the referral program to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "memberOffer": "string",
      "name": "Ava Chen",
      "referralOffer": "string",
      "title": "string",
      "type": "string",
      "widgetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directUrl` | string |  |
| `id` | string |  |
| `isActive` | boolean |  |
| `memberOffer` | string |  |
| `name` | string |  |
| `referralOffer` | string |  |
| `title` | string |  |
| `type` | string |  |
| `widgetUrl` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/program/getsingle` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-program.md) for the provider-specific parameters and requirements.

