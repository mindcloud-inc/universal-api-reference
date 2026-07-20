# Referral Rock: Delete Members

Deletes existing members from Referral Rock.

```
DELETE https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-members?connectionId=$CONNECTION_ID&items%5B%5D.query=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "items[].query": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-members?${params}`, {
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
| `items[]` | array<object> | no |  |
| `items[].query.primaryInfo.memberId` | string | no |  |
| `items[].query.primaryInfo.referralCode` | string | no |  |
| `items[].query.secondaryInfo.email` | string | no |  |
| `items[].query.secondaryInfo.externalIdentifier` | string | no |  |
| `items[].query.tertiaryInfo.programId` | string | no |  |
| `items[].query.tertiaryInfo.programName` | string | no |  |
| `items[].query.tertiaryInfo.programTitle` | string | no |  |
| `items[].query` | object | yes |  |
| `items[].query.primaryInfo` | object | no |  |
| `items[].query.secondaryInfo` | object | no |  |
| `items[].query.tertiaryInfo` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": {
        "primaryInfo": {
          "memberId": "string",
          "referralCode": {}
        },
        "secondaryInfo": {},
        "tertiaryInfo": {}
      },
      "resultInfo": {
        "message": {},
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `query.primaryInfo.memberId` | string |  |
| `query.primaryInfo.referralCode` | object |  |
| `query.secondaryInfo` | object |  |
| `query.tertiaryInfo` | object |  |
| `resultInfo.message` | object |  |
| `resultInfo.status` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/members/remove` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-members.md) for the provider-specific parameters and requirements.

