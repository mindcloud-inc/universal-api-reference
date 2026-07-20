# Click2Mail: Create Job

Creates a new job in Click2Mail.

```
POST https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentClass": "string",
  "layout": "string",
  "productionTime": "string",
  "envelope": "string",
  "color": "string",
  "paperType": "string",
  "printOption": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentClass": "string",
    "layout": "string",
    "productionTime": "string",
    "envelope": "string",
    "color": "string",
    "paperType": "string",
    "printOption": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentClass` | string | yes | The general type of the product |
| `layout` | string | yes | The specific type of the product |
| `productionTime` | string | yes | The desired production time |
| `envelope` | string | yes | If this is an enveloped product this determines the envelope in which the product is to be mailed; otherwise provide no value |
| `color` | string | yes | Print in color or black and white |
| `paperType` | string | yes | Sets the paper the mailing is to be printed on |
| `printOption` | string | yes | Sets simplex or duplex printing |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | no | ID of the document to print |
| `addressId` | string | no | This required if the product required a recipient address list |
| `rtnName` | string | no | Return address Name |
| `rtnOrganization` | string | no | Return address Organization |
| `rtnaddress1` | string | no | Return address line 1 |
| `rtnaddress2` | string | no | Return address line 2 |
| `rtnCity` | string | no | Return address City |
| `rtnState` | string | no | Return address state |
| `rtnZip` | string | no | Return address zip code |
| `endorsement` | string | no | Ancillary endorsement service, the default is none |
| `mailClass` | string | no | Overrides the default of First Class for mailed products |
| `appSignature` | string | no | This is a short signature to identify orders that come from your app |
| `projectId` | number | no | use to place this job in a pre-existing project in your account |
| `mailingDate` | string | no | Used to schedule the mailing date in the future. Format YYYYMMDD. If not provided the order will be mailed on the next available on the next business day. The business day cut off is 8PM EST. |
| `quantity` | string | no | For products that do not use mailing lists. Quantity to print |
| `jobDocumentId` | string | no | document ID of the job version of the document |
| `jobAddressId` | string | no | Address List Id of the job version |
| `businessReplyAddressId` | number | no | If you are mailing a business reply mail product use this to specify the busines reply address and permit information already in your account |
| `courtesyReplyAddressId` | number | no | If you are mailing a courtesy reply mail product use this to specify a courtesy reply address already in your account |
| `returnAddressId` | number | no | You may use the return address id to specify a return address already in your account |
| `enclosure` | string | no | Identifies the special encloure to use with this order. Special enclosures must be pre-arranged with Click2Mail |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `POST /molpro/jobs` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

