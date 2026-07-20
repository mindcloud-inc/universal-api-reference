# Google Ads: Mutate Resources

Creates, updates, or removes resources in Google Ads.

```
PUT https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/mutate-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/mutate-resources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/mutate-resources', {
  method: 'PUT',
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
| `customerId` | list | no |  |
| `mutateOperations[]` | array<object> | no | Required. The list of operations to perform on individual resources. |
| `partialFailure` | boolean | no | If true, successful operations will be carried out and invalid operations will return errors. If false, all operations will be carried out in one transaction if and only if they are all valid. Default is false. |
| `validateOnly` | boolean | no | If true, the request is validated but not executed. Only errors are returned, not results. |
| `responseContentType` | list | no | The response content type setting. Determines whether the mutable resource or just the resource name should be returned post mutation. The mutable resource will only be returned if the resource has the appropriate response field. For example, MutateCampaignResult.campaign. Default: `MUTABLE_RESOURCE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "descriptiveName": "Ava Chen",
        "id": "string",
        "resourceName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.descriptiveName` | string |  |
| `customer.id` | string |  |
| `customer.resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mutate-resources.md) for the provider-specific parameters and requirements.

