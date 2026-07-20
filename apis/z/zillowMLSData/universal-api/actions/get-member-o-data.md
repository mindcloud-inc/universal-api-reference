# Zillow MLS Data: Get member (OData)

Retrieves a member record from Zillow MLS Data using OData.

```
GET https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-member-o-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow MLS Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-member-o-data?connectionId=$CONNECTION_ID&dataset=string&memberKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "string",
  "memberKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowMLSData/latest/actions/get-member-o-data?${params}`, {
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
| `dataset` | string | yes | Bridge dataset code that contains the OData member. |
| `memberKey` | string | yes | OData member identifier from Bridge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BridgeModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "JobTitle": "string",
      "MemberCity": "string",
      "MemberFirstName": "Ava",
      "MemberFullName": "Ava Chen",
      "MemberKey": "string",
      "MemberLastName": "Chen",
      "MemberMlsId": "string",
      "MemberMobilePhone": "string",
      "MemberOfficePhone": "string",
      "MemberStateOrProvince": "string",
      "MemberStatus": "string",
      "MemberType": "string",
      "ModificationTimestamp": "2026-05-07T12:00:00.000Z",
      "OfficeKey": "string",
      "OfficeName": "Ava Chen",
      "OriginatingSystemName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BridgeModificationTimestamp` | date | Last Bridge-side modification timestamp. |
| `JobTitle` | string | Member job title. |
| `MemberCity` | string | Member city. |
| `MemberFirstName` | string | Member first name. |
| `MemberFullName` | string | Member full name. |
| `MemberKey` | string | Primary member key. |
| `MemberLastName` | string | Member last name. |
| `MemberMlsId` | string | MLS member identifier. |
| `MemberMobilePhone` | string | Member mobile phone. |
| `MemberOfficePhone` | string | Member office phone. |
| `MemberStateOrProvince` | string | Member state or province. |
| `MemberStatus` | string | Member status. |
| `MemberType` | string | Member type. |
| `ModificationTimestamp` | date | Last member modification timestamp. |
| `OfficeKey` | string | Associated office key. |
| `OfficeName` | string | Associated office name. |
| `OriginatingSystemName` | string | Originating system name. |

## Native endpoint

Through the native Zillow MLS Data API, this operation is `GET /OData/:dataset/Members(':memberKey')` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member-o-data.md) for the provider-specific parameters and requirements.

