# Preview SMS Message with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/1/preview`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Preview SMS Message](https://www.infobip.com/docs/api/channels/sms/outbound-sms/preview-sms-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Content of the message being sent. |
| `languageCode` | body | `string` | no | [Language code](https://www.infobip.com/docs/sms/language#national-language-identifier) for the correct character set. `AUTODETECT` lets the platform select the character set based on message content only for supported languages. |
| `transliteration` | body | `string` | no | The transliteration of your sent message from one script to another. [Transliteration](https://www.infobip.com/docs/sms/language#sms-transliteration) is used to replace characters which are not recognized as part of your defaulted alphabet. `ALL` means that the transliteration process will recognize all supported languages. |
