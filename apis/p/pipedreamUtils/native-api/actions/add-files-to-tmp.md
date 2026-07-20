# Add Files To /tmp with Pipedream Utils

Adds files to /tmp in Pipedream Utils.

## Endpoint

- **Method:** `GET`
- **Base URL:** `https://pipedream.com`
- **Official documentation:** [Add Files To /tmp](https://raw.githubusercontent.com/PipedreamHQ/pipedream/master/components/pipedream_utils/actions/add-files-to-tmp/add-files-to-tmp.mjs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files[]` | body | `array<string>` | yes | An array of file URLs or base64-encoded file contents |
