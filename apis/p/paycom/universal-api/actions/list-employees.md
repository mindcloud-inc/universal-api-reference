# Paycom: List Employees



```
GET https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycom/latest/actions/list-employees?${params}`, {
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
| `eestatus` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aptSuiteOther": "string",
      "cat1": "string",
      "cat10": "string",
      "cat10desc": "string",
      "cat11": "string",
      "cat11desc": "string",
      "cat12": "string",
      "cat12desc": "string",
      "cat13": "string",
      "cat13desc": "string",
      "cat14": "string",
      "cat14desc": "string",
      "cat15": "string",
      "cat15desc": "string",
      "cat16": "string",
      "cat16desc": "string",
      "cat17": "string",
      "cat17desc": "string",
      "cat18": "string",
      "cat18desc": "string",
      "cat19": "string",
      "cat19desc": "string",
      "cat1desc": "string",
      "cat2": "string",
      "cat20": "string",
      "cat20desc": "string",
      "cat2desc": "string",
      "cat3": "string",
      "cat3desc": "string",
      "cat4": "string",
      "cat4desc": "string",
      "cat5": "string",
      "cat5desc": "string",
      "cat6": "string",
      "cat6desc": "string",
      "cat7": "string",
      "cat7desc": "string",
      "cat8": "string",
      "cat8desc": "string",
      "cat9": "string",
      "cat9desc": "string",
      "cityaddr": "string",
      "clockseq": "string",
      "countryPaidIn": "string",
      "deptcode": "string",
      "deptdesc": "string",
      "eebadge": "string",
      "eecode": "string",
      "eename": "Ava Chen",
      "eestatus": "string",
      "firstname": "Ava",
      "gender": "string",
      "homephone": "string",
      "homephoneCountryCode": "string",
      "homestate": "string",
      "lastname": "Chen",
      "streetaddr": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aptSuiteOther` | string |  |
| `cat1` | string |  |
| `cat10` | string |  |
| `cat10desc` | string |  |
| `cat11` | string |  |
| `cat11desc` | string |  |
| `cat12` | string |  |
| `cat12desc` | string |  |
| `cat13` | string |  |
| `cat13desc` | string |  |
| `cat14` | string |  |
| `cat14desc` | string |  |
| `cat15` | string |  |
| `cat15desc` | string |  |
| `cat16` | string |  |
| `cat16desc` | string |  |
| `cat17` | string |  |
| `cat17desc` | string |  |
| `cat18` | string |  |
| `cat18desc` | string |  |
| `cat19` | string |  |
| `cat19desc` | string |  |
| `cat1desc` | string |  |
| `cat2` | string |  |
| `cat20` | string |  |
| `cat20desc` | string |  |
| `cat2desc` | string |  |
| `cat3` | string |  |
| `cat3desc` | string |  |
| `cat4` | string |  |
| `cat4desc` | string |  |
| `cat5` | string |  |
| `cat5desc` | string |  |
| `cat6` | string |  |
| `cat6desc` | string |  |
| `cat7` | string |  |
| `cat7desc` | string |  |
| `cat8` | string |  |
| `cat8desc` | string |  |
| `cat9` | string |  |
| `cat9desc` | string |  |
| `cityaddr` | string |  |
| `clockseq` | string |  |
| `countryPaidIn` | string |  |
| `deptcode` | string |  |
| `deptdesc` | string |  |
| `eebadge` | string |  |
| `eecode` | string |  |
| `eename` | string |  |
| `eestatus` | string |  |
| `firstname` | string |  |
| `gender` | string |  |
| `homephone` | string |  |
| `homephoneCountryCode` | string |  |
| `homestate` | string |  |
| `lastname` | string |  |
| `streetaddr` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Paycom API, this operation is `GET api/v1/employeedirectory` (base URL `https://api.paycomonline.net/v4/rest/index.php/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

