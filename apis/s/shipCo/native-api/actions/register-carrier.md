# Register Carrier with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/carriers`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Register Carrier](https://developer.shipandco.com/en/#carrier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Carrier type such as dhl, fedex, japanpost, sagawa, yamato, yuupack, yuupacket, yuumail, or seino. |
| `credentials` | body | `object` | yes | Carrier credentials object. Required fields vary by carrier. |
| `settings` | body | `object` | no | Carrier settings object, including print settings where required. |
