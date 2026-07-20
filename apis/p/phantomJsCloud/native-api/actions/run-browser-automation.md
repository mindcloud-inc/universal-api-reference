# Run Browser Automation with PhantomJsCloud

Runs browser automation in PhantomJsCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/:apiKey/`
- **Base URL:** `https://phantomjscloud.com/api/browser/v2`
- **Official documentation:** [Run Browser Automation](https://phantomjscloud.com/docs/http-api/automation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Optional starting URL for the automation request. |
| `overseerScript` | body | `string` | yes | The automation script to run in PhantomJsCloud. |
