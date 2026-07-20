# DynamicPDF: Extract PDF Page Range

Extracts a page range from a PDF in DynamicPDF API.

```
GET https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/extract-pdf-page-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/extract-pdf-page-range?connectionId=$CONNECTION_ID&instructions=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instructions": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/extract-pdf-page-range?${params}`, {
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
| `instructions` | object | yes | DynamicPDF instructions document sent as raw JSON. Default: `{"title":"Extract PDF Page Range","author":"MindCloud","inputs":[{"type":"pdf","pageCount":1,"startPage":2,"resourceName":"base.pdf"}],"creator":"DynamicPDF API","resources":[{"data":"JVBERi0xLjcKJeLjz9MKMSAwIG9iago8PC9BdXRob3IoTWluZENsb3VkKS9DcmVhdG9yKER5bmFtaWNQREYgQVBJKS9LZXl3b3JkcyhtaW5kY2xvdWQsZHluYW1pY3BkZixzdGFnZTMpL1N1YmplY3QoU3RhZ2UgMyByZXVzYWJsZSBmaXh0dXJlKS9UaXRsZShNaW5kQ2xvdWQgRHluYW1pY1BERiBTdGFnZSAzIEJhc2UgUERGKS9Qcm9kdWNlcihEeW5hbWljUERGIEFQSSB2MSBcKEJ1aWxkIDU1Nzk3XCkpL0NyZWF0aW9uRGF0ZShEOjIwMjYwNDAxMTkxMTAwKzAwJzAwJykvTW9kRGF0ZShEOjIwMjYwNDAxMTkxMTAwKzAwJzAwJyk+PgplbmRvYmoKMiAwIG9iago8PC9UeXBlL1BhZ2VzL0tpZHNbMyAwIFIgNCAwIFIgNSAwIFJdL0NvdW50IDM+PgplbmRvYmoKMyAwIG9iago8PC9UeXBlL1BhZ2UvUGFyZW50IDIgMCBSL01lZGlhQm94WzAgMCA2MTIgNzkyXS9Db250ZW50cyA3IDAgUi9Bbm5vdHNbOCAwIFJdL1Jlc291cmNlczw8L1Byb2NTZXRbL1BERi9JbWFnZUMvSW1hZ2VJL0ltYWdlQi9UZXh0XS9Gb250PDwvRjAgOSAwIFI+Pj4+Pj4KZW5kb2JqCjQgMCBvYmoKPDwvVHlwZS9QYWdlL1BhcmVudCAyIDAgUi9NZWRpYUJveFswIDAgNjEyIDc5Ml0vQ29udGVudHMgMTAgMCBSL0Fubm90c1sxMSAwIFJdL1Jlc291cmNlczw8L1Byb2NTZXRbL1BERi9JbWFnZUMvSW1hZ2VJL0ltYWdlQi9UZXh0XS9Gb250PDwvRjAgOSAwIFI+Pj4+Pj4KZW5kb2JqCjUgMCBvYmoKPDwvVHlwZS9QYWdlL1BhcmVudCAyIDAgUi9NZWRpYUJveFswIDAgNjEyIDc5Ml0vQ29udGVudHMgMTIgMCBSL0Fubm90c1sxMyAwIFJdL1Jlc291cmNlczw8L1Byb2NTZXRbL1BERi9JbWFnZUMvSW1hZ2VJL0ltYWdlQi9UZXh0XS9Gb250PDwvRjAgOSAwIFI+Pj4+Pj4KZW5kb2JqCjYgMCBvYmoKPDwvVHlwZS9DYXRhbG9nL1BhZ2VzIDIgMCBSL1BhZ2VMYXlvdXQvU2luZ2xlUGFnZS9QYWdlTGFiZWxzPDwvTnVtc1swPDwvUy9EPj4xPDwvUy9EPj4yPDwvUy9EPj5dPj4vT3BlbkFjdGlvblszIDAgUi9YWVogbnVsbCBudWxsIG51bGxdPj4KZW5kb2JqCjcgMCBvYmoKPDwvRmlsdGVyL0ZsYXRlRGVjb2RlL0xlbmd0aCAyMDg+PnN0cmVhbQp4nGWPy27CMBBF9/6Ku2tZ1NgOeS1LAQmJRQT+AUMnwRUkkmMU+HvsUKpKaHYzmnPPFYjjGjbXbLoSUAq6ZirlCfSGyfEqkQrks5yn0Gf2vvOmISSYm55QLVb4QBU3cvI2IuSIkAkvXhAPwJYuvdmfCP7ousEM5obaXv3FEerOYXFrzdkeItkcvO1aeOq9bRseApY6EOMEZYEhmJa8LJDzrECpuFDIeK7giNXPSlnU+ev59Pl9LEejL0fG0zcG64/Biv47fFbrif6JwXcIS0u9CmVuZHN0cmVhbQplbmRvYmoKOCAwIG9iago8PC9UeXBlL0Fubm90L1N1YnR5cGUvTGluay9Cb3JkZXJbMCAwIDBdL0E8PC9UeXBlL0FjdGlvbi9TL1VSSS9VUkkoaHR0cHM6Ly9kcGRmLmlvKT4+L0YgNC9SZWN0WzI1OS45OCA3LjY3IDM1Mi4wMSAxNC40XT4+CmVuZG9iago5IDAgb2JqCjw8L1R5cGUvRm9udC9TdWJ0eXBlL1R5cGUxL0Jhc2VGb250L0hlbHZldGljYS9FbmNvZGluZy9XaW5BbnNpRW5jb2Rpbmc+PgplbmRvYmoKMTAgMCBvYmoKPDwvRmlsdGVyL0ZsYXRlRGVjb2RlL0xlbmd0aCAyMTE+PnN0cmVhbQp4nGWPy27CMBBF9/6Ku2uRqOs45LUkUCQkFpHqH7CSCaQiCXJGAv4eO4Ju0Ozmas6cqxDGHUVpxPdOQWuYVuhExjAHEc1phEQhW2UygenF5y/bIyFGaSdCtd3hC1XY6MXHjIhmRBTL/A3xBFA9Dg0u4agdHabLueMlGjoT0xLWZ84OPqQbO1tzNw5gmniS/sOP8cgw3lnh6lULWeTIZJqj0FJppDLTcCTaV6c0+PwXfQk9D4tZaePIMjW4dnwCnwjb+2D7rg711tV+Yf7C4wfktktnCmVuZHN0cmVhbQplbmRvYmoKMTEgMCBvYmoKPDwvVHlwZS9Bbm5vdC9TdWJ0eXBlL0xpbmsvQm9yZGVyWzAgMCAwXS9BPDwvVHlwZS9BY3Rpb24vUy9VUkkvVVJJKGh0dHBzOi8vZHBkZi5pbyk+Pi9GIDQvUmVjdFsyNTkuOTggNy42NyAzNTIuMDEgMTQuNF0+PgplbmRvYmoKMTIgMCBvYmoKPDwvRmlsdGVyL0ZsYXRlRGVjb2RlL0xlbmd0aCAxOTQ+PnN0cmVhbQp4nGWPyw6CMBRE9/2K2SkLaynyWoqPxMQFif0BIuVhRE25xPj30ipuzOzuzZyZEbAyNcsUW+4FpISqmAx5AHVkvvv6CAXiVcxDqI7NT1TUGgGyotfIt3sskLuLN3MI3yH8gCd/iA9ANa0p8bCe6m7QDVdqF/eBHgOBdE89H0k7NVqtxm4Cz7FSytMEMY8SpJILiYjHEkazauoe2dzfoCn4a0xd9MbognSJZ0sNqNHYvm5F157tjHV+8NTFBr8B7/RDGAplbmRzdHJlYW0KZW5kb2JqCjEzIDAgb2JqCjw8L1R5cGUvQW5ub3QvU3VidHlwZS9MaW5rL0JvcmRlclswIDAgMF0vQTw8L1R5cGUvQWN0aW9uL1MvVVJJL1VSSShodHRwczovL2RwZGYuaW8pPj4vRiA0L1JlY3RbMjU5Ljk4IDcuNjcgMzUyLjAxIDE0LjRdPj4KZW5kb2JqCjE0IDAgb2JqCjw8L1R5cGUvWFJlZi9XWzEgMiAwXS9EZWNvZGVQYXJtczw8L0NvbHVtbnMgMy9QcmVkaWN0b3IgMTI+Pi9GaWx0ZXIvRmxhdGVEZWNvZGUvTGVuZ3RoIDU3L1NpemUgMTQvUm9vdCA2IDAgUi9JbmZvIDEgMCBSL0lEWzxkODliNTQ3NTFkZDBhYzRlOTg2ZTM5NjY0N2M3NjRjNz48ZDg5YjU0NzUxZGQwYWM0ZTk4NmUzOTY2NDdjNzY0Yzc+XT4+c3RyZWFtCnicFcixFQAQEATRtYFUINCBNrShJdeBBjxlGsF/c7eW5KRipc496KGXfhuVf2FabjTYMuIBjfkFUQplbmRzdHJlYW0KZW5kb2JqCgpzdGFydHhyZWYKMjM0NAolJUVPRgo=","name":"base.pdf"}]}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-pdf-page-range.md) for the provider-specific parameters and requirements.

