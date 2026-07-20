# List Subscribers with Clever Elements

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `http://api.sendcockpit.com/server.php`
- **Official documentation:** [List Subscribers](https://docs.cleverelements.com/kb/api/#document-9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `soapenv:Envelope.soapenv:Body.sen:apiGetSubscriber.ctListRequest.listID` | body | `string` | yes | The Clever Elements list ID. |
| `soapenv:Envelope.soapenv:Body.sen:apiGetSubscriber.ctListRequest.start` | body | `string` | no | Zero-based start offset. |
| `soapenv:Envelope.soapenv:Body.sen:apiGetSubscriber.ctListRequest.count` | body | `string` | no | Maximum number of subscribers to return. |
