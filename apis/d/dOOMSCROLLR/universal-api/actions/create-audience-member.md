# DOOMSCROLLR: Create Audience Member



```
POST https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-audience-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DOOMSCROLLR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-audience-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dOOMSCROLLR/latest/actions/create-audience-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Audience member email address. Example: `user@example.com`. |
| `firstName` | string | no | Audience member first name. Example: `John`. |
| `lastName` | string | no | Audience member last name. Example: `Doe`. |
| `phone` | string | no | Audience member phone number. Example: `+1234567890`. |
| `gender` | string | no | Audience member gender. Example: `M`. |
| `source` | string | no | Source label for how the audience member was acquired. Example: `email_signup`. |
| `city` | string | no | Audience member city. Example: `Los Angeles`. |
| `state` | string | no | Audience member state or region. Example: `California`. |
| `country` | string | no | Audience member country. Example: `United States`. |
| `bio` | string | no | Audience member biography or descriptor. Example: `Creative Director`. |
| `username` | string | no | Audience member username or handle. Example: `johndoe123`. |
| `followers` | number | no | Follower count for the audience member. Example: `10000000`. |
| `tags[]` | array<string> | no | Tags to assign to the audience member. Accepts multiple values as an array. Example: `fashion,design,luxury`. |
| `utmSource` | string | no | UTM source for the audience member attribution. Example: `doomscrollr`. |
| `utmMedium` | string | no | UTM medium for the audience member attribution. Example: `social`. |
| `utmCampaign` | string | no | UTM campaign for the audience member attribution. Example: `spring_sale_2025`. |
| `utmContent` | string | no | UTM content value for the audience member attribution. Example: `carousel_ad_1`. |
| `utmTerm` | string | no | UTM term value for the audience member attribution. Example: `trendy_jackets`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailMd5` | string | no | MD5 hash of the lowercase email address when email is not provided. Example: `b58996c504c5638798eb6b511e6f49af`. |
| `createdAt` | string | no | Optional created-at timestamp from the official Postman collection. Example: `2025-02-10T02:25:23.000000Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DOOMSCROLLR API returns.

## Native endpoint

Through the native DOOMSCROLLR API, this operation is `POST /api/audience/create` (base URL `https://mindcloudapps0402.doomscrollr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audience-member.md) for the provider-specific parameters and requirements.

