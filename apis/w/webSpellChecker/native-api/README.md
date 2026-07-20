# WebSpellChecker: Native API Reference

A consolidated summary of WebSpellChecker's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Using%2BCloud%2BWebSpellChecker%2BAPI
- **API base URL:** `https://svc.webspellchecker.net/api`

## Authentication

### Service ID

Passes the WebSpellChecker Cloud service ID as the required customerid request parameter.

### Credentials

- **Service ID:** `customerid` · required · Your WebSpellChecker Cloud service ID.

[Official authentication documentation](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Using%2BCloud%2BWebSpellChecker%2BAPI)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User Dictionary Word](actions/add-user-dictionary-word.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Using%2BWebSpellChecker%2BServer%2BWeb%2BAPI) |
| [Add User Dictionary Words](actions/add-user-dictionary-words.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Check Spelling](actions/check-spelling.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Check%2Bspelling%2Bcommand) |
| [Check Text](actions/check-text.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Using%2BCloud%2BWebSpellChecker%2BAPI) |
| [Check User Dictionary](actions/check-user-dictionary.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Create User Dictionary](actions/create-user-dictionary.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Delete User Dictionary](actions/delete-user-dictionary.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Delete User Dictionary Word](actions/delete-user-dictionary-word.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Using%2BWebSpellChecker%2BServer%2BWeb%2BAPI) |
| [Delete User Dictionary Words](actions/delete-user-dictionary-words.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Detect Language](actions/detect-language.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Detect%2Blanguage%2Bcommand) |
| [Edit User Dictionary Word](actions/edit-user-dictionary-word.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Get Info](actions/get-info.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Get%2Binfo%2Bcommand) |
| [Get Language List](actions/get-language-list.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Using%2BWebSpellChecker%2BServer%2BWeb%2BAPI) |
| [Get Status](actions/get-status.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Installing%2BWebSpellChecker%2Bon%2BLinux%2Bwith%2BApache%2BHTTP%2BServer) |
| [Get User Dictionary](actions/get-user-dictionary.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
| [Get Version](actions/get-version.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerServer55x/Installing%2BWebSpellChecker%2Bon%2BLinux%2Bwith%2BApache%2BHTTP%2BServer) |
| [Grammar Check](actions/grammar-check.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/Grammar%2Bcheck%2Bcommand) |
| [Rename User Dictionary](actions/rename-user-dictionary.md) | `GET /` | [docs](https://docs.webspellchecker.com/display/WebSpellCheckerCloud/User%2Bdictionary%2Bcommand) |
