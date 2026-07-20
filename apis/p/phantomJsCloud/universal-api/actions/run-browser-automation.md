# PhantomJsCloud: Run Browser Automation

Runs browser automation in PhantomJsCloud.

```
GET https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/run-browser-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomJsCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/run-browser-automation?connectionId=$CONNECTION_ID&overseerScript=await%20page.waitForNavigation(%7BwaitUntil%3A%22domcontentloaded%22%7D)%3B%20await%20page.meta.log(await%20page.content(%7Bselector%3A%22button%23dateBtn%22%2Ctype%3A%22plainText%22%7D))%3B%20page.click(%22button%23dateBtn%22)%3B%20await%20page.waitForFunction(()%3D%3Edocument.querySelector(%22%23demo_result%22).textContent.length%3E0)%3B%20await%20page.meta.log(await%20page.content(%7Bselector%3A%22%23demo_result%22%2Ctype%3A%22plainText%22%7D))%3B" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "overseerScript": "await page.waitForNavigation({waitUntil:\"domcontentloaded\"}); await page.meta.log(await page.content({selector:\"button#dateBtn\",type:\"plainText\"})); page.click(\"button#dateBtn\"); await page.waitForFunction(()=>document.querySelector(\"#demo_result\").textContent.length>0); await page.meta.log(await page.content({selector:\"#demo_result\",type:\"plainText\"}));"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomJsCloud/latest/actions/run-browser-automation?${params}`, {
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
| `url` | string | no | Optional starting URL for the automation request. Default: `https://phantomjscloud.com/static-samples/button-click.html`. |
| `overseerScript` | string | yes | The automation script to run in PhantomJsCloud. Default: `await page.waitForNavigation({waitUntil:\"domcontentloaded\"}); await page.meta.log(await page.content({selector:\"button#dateBtn\",type:\"plainText\"})); page.click(\"button#dateBtn\"); await page.waitForFunction(()=>document.querySelector(\"#demo_result\").textContent.length>0); await page.meta.log(await page.content({selector:\"#demo_result\",type:\"plainText\"}));`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "logs": [
        {
          "time": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ],
      "renders": [
        {}
      ],
      "storage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Automation error entries. |
| `logs` | array<object> | Automation log entries. |
| `logs[].time` | date | Timestamp for one automation log entry. |
| `logs[].value` | string | Logged output value. |
| `renders` | array<object> | Rendered output entries captured during automation. |
| `storage` | object | Stored automation key-value output. |

## Native endpoint

Through the native PhantomJsCloud API, this operation is `POST /:apiKey/` (base URL `https://phantomjscloud.com/api/browser/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-browser-automation.md) for the provider-specific parameters and requirements.

