# Create Print Job with PrintNode

Creates a new print job in PrintNode.

## Endpoint

- **Method:** `POST`
- **Path:** `/printjobs`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Create Print Job](https://www.printnode.com/en/docs/api/curl#printjob-creating)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `printerId` | body | `number` | yes | The ID of the printer you want to print to. |
| `contentType` | body | `string` | yes | One of pdf_uri, pdf_base64, raw_uri, or raw_base64. |
| `content` | body | `string` | yes | A document URI or a base64-encoded document, depending on contentType. |
| `title` | body | `string` | no | Optional print queue title. |
| `source` | body | `string` | no | Optional description of where the print job originated. |
| `options` | body | `object` | no | Optional object of PrintNode print options, such as copies, pages, duplex, paper, or bin. |
| `expireAfter` | body | `number` | no | Optional maximum number of seconds PrintNode should retain the print job before expiry. |
| `qty` | body | `number` | no | Optional number of times the print job should be delivered to the queue. |
| `authentication` | body | `object` | no | Optional HTTP Basic or Digest authentication object used when PrintNode must download the document from a protected URI. |
