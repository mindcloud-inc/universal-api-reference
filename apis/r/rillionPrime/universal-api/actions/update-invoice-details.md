# Rillion Prime: Update Invoice Details



```
PUT https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceDetail": {},
  "invoiceDetailHeadersOnly": 1,
  "invoiceDetailForProcessing": true,
  "invoiceDetailLocked": true,
  "invoiceDetailLockedRowId": 1,
  "invoiceDetailLockedRowLoginName": "Ava Chen",
  "invoiceDetailLockedRowRole": "string",
  "invoiceDetailRowState": 1,
  "invoiceDetailSelected": true,
  "invoiceDetailKeyValuesRowState": 1,
  "invoiceDetailInvoice": {},
  "invoiceDetailInvoiceHeadersOnly": 1,
  "invoiceDetailInvoiceForProcessing": true,
  "invoiceDetailInvoiceLocked": true,
  "invoiceDetailInvoiceLockedRowId": 1,
  "invoiceDetailInvoiceLockedRowLoginName": "Ava Chen",
  "invoiceDetailInvoiceLockedRowRole": "string",
  "invoiceDetailInvoiceRowState": 1,
  "invoiceDetailInvoiceSelected": true,
  "invoiceDetailInvoiceKeyValuesRowState": 1,
  "invoiceDetailInvoiceAccount": "string",
  "invoiceDetailInvoiceAccountCodingDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceAccountCodingProposal": "string",
  "invoiceDetailInvoiceAccountCodingProposalID": 1,
  "invoiceDetailInvoiceAccountId": 1,
  "invoiceDetailInvoiceAccountName": "Ava Chen",
  "invoiceDetailInvoiceAlternativeId": "string",
  "invoiceDetailInvoiceAmount": 1,
  "invoiceDetailInvoiceArrivalAccountCoded": true,
  "invoiceDetailInvoiceArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceArrivalDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceArrivalTime": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceAsset": true,
  "invoiceDetailInvoiceAuthorizationRole": "string",
  "invoiceDetailInvoiceAuthorizationUser": "string",
  "invoiceDetailInvoiceBaseAmount": 1,
  "invoiceDetailInvoiceBaseCurrency": "string",
  "invoiceDetailInvoiceBaseNetAmount": 1,
  "invoiceDetailInvoiceBaseVatAmount": 1,
  "invoiceDetailInvoiceBlocked": true,
  "invoiceDetailInvoiceBuyingRate": 1,
  "invoiceDetailInvoiceChTime": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceChUser": "string",
  "invoiceDetailInvoiceClassified": true,
  "invoiceDetailInvoiceCompany": "string",
  "invoiceDetailInvoiceCompanyDTO": {},
  "invoiceDetailInvoiceCompanyDTOHeadersOnly": 1,
  "invoiceDetailInvoiceCompanyDTOForProcessing": true,
  "invoiceDetailInvoiceCompanyDTOLocked": true,
  "invoiceDetailInvoiceCompanyDTOLockedRowId": 1,
  "invoiceDetailInvoiceCompanyDTOLockedRowLoginName": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOLockedRowRole": "string",
  "invoiceDetailInvoiceCompanyDTORowState": 1,
  "invoiceDetailInvoiceCompanyDTOSelected": true,
  "invoiceDetailInvoiceCompanyDTOKeyValuesRowState": 1,
  "invoiceDetailInvoiceCompanyDTOCompany": "string",
  "invoiceDetailInvoiceCompanyDTOName": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOType": "string",
  "invoiceDetailInvoiceCompanyDTOValidTo": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceCompanyDTOInvoiceSeries": "string",
  "invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries": "string",
  "invoiceDetailInvoiceCompanyDTOBaseCurrency": "string",
  "invoiceDetailInvoiceCompanyDTOVatNo": "string",
  "invoiceDetailInvoiceCompanyDTOPostalAddressId": 1,
  "invoiceDetailInvoiceCompanyDTOWww": "string",
  "invoiceDetailInvoiceCompanyDTOContact": "string",
  "invoiceDetailInvoiceCompanyDTOEmail": "ava@example.com",
  "invoiceDetailInvoiceCompanyDTOErrorHandlingRole": "string",
  "invoiceDetailInvoiceCompanyDTOCheckRange": 1,
  "invoiceDetailInvoiceCompanyDTOCheckCounter": 1,
  "invoiceDetailInvoiceCompanyDTOCheckRole": "string",
  "invoiceDetailInvoiceCompanyDTOCodeRelationIsActive": true,
  "invoiceDetailInvoiceCompanyDTOCodeRelationCheckType": "string",
  "invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck": "string",
  "invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck": true,
  "invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck": true,
  "invoiceDetailInvoiceCompanyDTOArrivalType": "string",
  "invoiceDetailInvoiceCompanyDTOArrivalAccountCoding": "string",
  "invoiceDetailInvoiceCompanyDTOAccountCodingDate": "string",
  "invoiceDetailInvoiceCompanyDTOCalculateDueDate": "string",
  "invoiceDetailInvoiceCompanyDTOSetAccountCodedBy": true,
  "invoiceDetailInvoiceCompanyDTOFlowProposalId": 1,
  "invoiceDetailInvoiceCompanyDTOPaymentTermId": 1,
  "invoiceDetailInvoiceCompanyDTOAllocationsAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOClassifySupplier": true,
  "invoiceDetailInvoiceCompanyDTODebtAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOCostAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOVatAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat": true,
  "invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles": 1,
  "invoiceDetailInvoiceCompanyDTOSigningRule": "string",
  "invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign": true,
  "invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending": true,
  "invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit": 1,
  "invoiceDetailInvoiceCompanyDTOGetVatCodeFrom": "string",
  "invoiceDetailInvoiceCompanyDTOVatAccountCodingType": 1,
  "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo": 1,
  "invoiceDetailInvoiceCompanyDTOFlowAtUnknown": "string",
  "invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown": 1,
  "invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown": "string",
  "invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown": 1,
  "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown": "string",
  "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown": 1,
  "invoiceDetailInvoiceCompanyDTOUseReference": "string",
  "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow": 1,
  "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed": 1,
  "invoiceDetailInvoiceCompanyDTOAutoDelivery": true,
  "invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder": "string",
  "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder": "string",
  "invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder": "string",
  "invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays": 1,
  "invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail": "ava@example.com",
  "invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays": 1,
  "invoiceDetailInvoiceCompanyDTOReMatchPriceEmail": "ava@example.com",
  "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed": 1,
  "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow": 1,
  "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount": 1,
  "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1": 1,
  "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2": 1,
  "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3": 1,
  "invoiceDetailInvoiceCompanyDTOMaxFeeAmount1": 1,
  "invoiceDetailInvoiceCompanyDTOMaxFeeAmount2": 1,
  "invoiceDetailInvoiceCompanyDTOMaxFeeAmount3": 1,
  "invoiceDetailInvoiceCompanyDTOErp": "string",
  "invoiceDetailInvoiceCompanyDTOGroup1": "string",
  "invoiceDetailInvoiceCompanyDTOGroup2": "string",
  "invoiceDetailInvoiceCompanyDTOGroup3": "string",
  "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign": true,
  "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder": true,
  "invoiceDetailInvoiceCompanyDTOChTime": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceCompanyDTOChUser": "string",
  "invoiceDetailInvoiceCompanyDTODirectRecording": true,
  "invoiceDetailInvoiceCompanyDTOVatExempt": true,
  "invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding": true,
  "invoiceDetailInvoiceCompanyDTOIdentifyBitCode": 1,
  "invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier": true,
  "invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder": "string",
  "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder": 1,
  "invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates": 1,
  "invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance": 1,
  "invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver": "string",
  "invoiceDetailInvoiceCompanyDTOExpenseInstantReminder": "string",
  "invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId": 1,
  "invoiceDetailInvoiceCompanyDTOExpenseSigningRule": "string",
  "invoiceDetailInvoiceCompanyDTORequisitionNoApproval": 1,
  "invoiceDetailInvoiceCompanyDTOEan": "string",
  "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount": true,
  "invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount": "string",
  "invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines": "string",
  "invoiceDetailInvoiceCompanyDTOUseBuyersHelp": true,
  "invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount": true,
  "invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval": true,
  "invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit": true,
  "invoiceDetailInvoiceCompanyDTOObjectType1Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType2Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType3Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType4Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType5Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType6Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType7Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOObjectType8Name": "Ava Chen",
  "invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote": true,
  "invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch": true,
  "invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote": true,
  "invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses": true,
  "invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown": "string",
  "invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown": 1,
  "invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery": true,
  "invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired": true,
  "invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat": "string",
  "invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval": "string",
  "invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount": true,
  "invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries": "string",
  "invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval": true,
  "invoiceDetailInvoiceCompanyDTODeliveryCode": "string",
  "invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat": true,
  "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting": "string",
  "invoiceDetailInvoiceCompanyDTOAllocationSetting": "string",
  "invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine": true,
  "invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately": true,
  "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting": "string",
  "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting": "string",
  "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting": true,
  "invoiceDetailInvoiceCompanyDTOAiInvoice": "string",
  "invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer": "string",
  "invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate": true,
  "invoiceDetailInvoiceCompanyDTOSupplierMatchPattern": "string",
  "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2": 1,
  "invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns": true,
  "invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType": "string",
  "invoiceDetailInvoiceCompanyDTOVarianceVatAccountId": 1,
  "invoiceDetailInvoiceCompanyDTOMaxVarianceAmount": 1,
  "invoiceDetailInvoiceCompanyDTOAiNoPrediction": "string",
  "invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter": true,
  "invoiceDetailInvoiceCompanyDTOVat1AccountId": 1,
  "invoiceDetailInvoiceCompanyDTOVat2AccountId": 1,
  "invoiceDetailInvoiceCompanyDTOVat3AccountId": 1,
  "invoiceDetailInvoiceCompanyDTOVat4AccountId": 1,
  "invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult": "string",
  "invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching": true,
  "invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation": "string",
  "invoiceDetailInvoiceCompanyDTOContractNoregexValidation": "string",
  "invoiceDetailInvoiceCompanyDTORillionCaptureUrl": "https://example.com",
  "invoiceDetailInvoiceCompanyDTORillionCapturelabel": "string",
  "invoiceDetailInvoiceCompanyDTOEInvoiceUrl": "https://example.com",
  "invoiceDetailInvoiceCompanyDTOEInvoiceLabel": "string",
  "invoiceDetailInvoiceCompanyDTOUseAmountInRounding": true,
  "invoiceDetailInvoiceCompanyDTORoundingAmount": 1,
  "invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate": true,
  "invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting": 1,
  "invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod": true,
  "invoiceDetailInvoiceCompanyDTOCompanyAlias": [
    "string"
  ],
  "invoiceDetailInvoiceCompanyName": "Ava Chen",
  "invoiceDetailInvoiceContractMatch": 1,
  "invoiceDetailInvoiceContractNo": "string",
  "invoiceDetailInvoiceCrDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceCredit": true,
  "invoiceDetailInvoiceCreditTime": 1,
  "invoiceDetailInvoiceCurrency": "string",
  "invoiceDetailInvoiceCurrentLevel": 1,
  "invoiceDetailInvoiceCurrentRole": "string",
  "invoiceDetailInvoiceDeptAccountId": 1,
  "invoiceDetailInvoiceDiscountAmount": 1,
  "invoiceDetailInvoiceDiscountDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceDiscountGrossAmount": true,
  "invoiceDetailInvoiceDiscountPercentage": 1,
  "invoiceDetailInvoiceDueDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceEmailSignRole": "ava@example.com",
  "invoiceDetailInvoiceExchangeRate": 1,
  "invoiceDetailInvoiceSystemCurrencyExchangeRate": 1,
  "invoiceDetailInvoiceExpenseMatch": 1,
  "invoiceDetailInvoiceExtraAmount": 1,
  "invoiceDetailInvoiceExtraId": "string",
  "invoiceDetailInvoiceFeeAmount1": 1,
  "invoiceDetailInvoiceFeeAmount2": 1,
  "invoiceDetailInvoiceFeeAmount3": 1,
  "invoiceDetailInvoiceFileTypeId": 1,
  "invoiceDetailInvoiceFlowAddition": 1,
  "invoiceDetailInvoiceFlowProposal": "string",
  "invoiceDetailInvoiceFlowProposalId": 1,
  "invoiceDetailInvoiceFlowStatus": 1,
  "invoiceDetailInvoiceForPartialPayment": true,
  "invoiceDetailInvoiceGroup1": "string",
  "invoiceDetailInvoiceGroup2": "string",
  "invoiceDetailInvoiceGroup3": "string",
  "invoiceDetailInvoiceGroup4": "string",
  "invoiceDetailInvoiceGroup5": "string",
  "invoiceDetailInvoiceGroup6": "string",
  "invoiceDetailInvoiceInvestigate": true,
  "invoiceDetailInvoiceInvoiceAccountCodingAmount": 1,
  "invoiceDetailInvoiceInvoiceDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceInvoiceFlowId": 1,
  "invoiceDetailInvoiceInvoiceFlowStatus": 1,
  "invoiceDetailInvoiceInvoiceId": 1,
  "invoiceDetailInvoiceInvoiceImageFileExtension": "string",
  "invoiceDetailInvoiceInvoiceNo": 1,
  "invoiceDetailInvoiceInvoiceSeries": "string",
  "invoiceDetailInvoiceInvoiceStatusMessage": "string",
  "invoiceDetailInvoiceIsContractMatch": 1,
  "invoiceDetailInvoiceIsPurchaseOrderMatch": 1,
  "invoiceDetailInvoiceLatestDiaryNote": "string",
  "invoiceDetailInvoiceLatestDiaryNoteUser": "string",
  "invoiceDetailInvoiceLatestDiaryNoteTime": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceLinkedInvoiceId": 1,
  "invoiceDetailInvoiceLinkedInvoiceNo": 1,
  "invoiceDetailInvoiceLinkedInvoiceSeries": "https://example.com",
  "invoiceDetailInvoiceMatchedContractId": 1,
  "invoiceDetailInvoiceNetAmount": 1,
  "invoiceDetailInvoiceNoOfRoles": 1,
  "invoiceDetailInvoiceObject1": "string",
  "invoiceDetailInvoiceObject1Id": 1,
  "invoiceDetailInvoiceObject1Name": "Ava Chen",
  "invoiceDetailInvoiceObject2": "string",
  "invoiceDetailInvoiceObject2Id": 1,
  "invoiceDetailInvoiceObject2Name": "Ava Chen",
  "invoiceDetailInvoiceObject3": "string",
  "invoiceDetailInvoiceObject3Id": 1,
  "invoiceDetailInvoiceObject3Name": "Ava Chen",
  "invoiceDetailInvoiceObject4": "string",
  "invoiceDetailInvoiceObject4Id": 1,
  "invoiceDetailInvoiceObject4Name": "Ava Chen",
  "invoiceDetailInvoiceObject5": "string",
  "invoiceDetailInvoiceObject5Id": 1,
  "invoiceDetailInvoiceObject5Name": "Ava Chen",
  "invoiceDetailInvoiceObject6": "string",
  "invoiceDetailInvoiceObject6Id": 1,
  "invoiceDetailInvoiceObject6Name": "Ava Chen",
  "invoiceDetailInvoiceObject7": "string",
  "invoiceDetailInvoiceObject7Id": 1,
  "invoiceDetailInvoiceObject7Name": "Ava Chen",
  "invoiceDetailInvoiceObject8": "string",
  "invoiceDetailInvoiceObject8Id": 1,
  "invoiceDetailInvoiceObject8Name": "Ava Chen",
  "invoiceDetailInvoiceOldAccountCodingDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceOriginalSupplierId": 1,
  "invoiceDetailInvoiceOriginalSupplierName": "Ava Chen",
  "invoiceDetailInvoiceOriginalVatType": "string",
  "invoiceDetailInvoicePartialPaymentAmount": 1,
  "invoiceDetailInvoicePartialPaymentAmountUpdated": true,
  "invoiceDetailInvoicePaymentDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoicePaymentMessage": "string",
  "invoiceDetailInvoicePaymentTerm": "string",
  "invoiceDetailInvoicePaymentTermId": 1,
  "invoiceDetailInvoicePaymentTime": 1,
  "invoiceDetailInvoicePayReference": "string",
  "invoiceDetailInvoicePeriodAmount": 1,
  "invoiceDetailInvoicePostingsUpdated": true,
  "invoiceDetailInvoiceProcessDays": 1,
  "invoiceDetailInvoiceProcessTime": 1,
  "invoiceDetailInvoicePurchaseOrderMatch": 1,
  "invoiceDetailInvoicePurchaseOrderNo": "string",
  "invoiceDetailInvoiceReference1": "string",
  "invoiceDetailInvoiceReference2": "string",
  "invoiceDetailInvoiceRemainingPartialPaymentAmount": 1,
  "invoiceDetailInvoiceReminderReason": 1,
  "invoiceDetailInvoiceRole": "string",
  "invoiceDetailInvoiceShowDate": "2026-05-07T12:00:00.000Z",
  "invoiceDetailInvoiceStatus": 1,
  "invoiceDetailInvoiceSupplier": "string",
  "invoiceDetailInvoiceSupplierActiveCreditCard": true,
  "invoiceDetailInvoiceSupplierAddress1": "string",
  "invoiceDetailInvoiceSupplierAddress2": "string",
  "invoiceDetailInvoiceSupplierAddress3": "string",
  "invoiceDetailInvoiceSupplierAddress4": "string",
  "invoiceDetailInvoiceSupplierAddress5": "string",
  "invoiceDetailInvoiceSupplierAddress6": "string",
  "invoiceDetailInvoiceSupplierBankAccount": "string",
  "invoiceDetailInvoiceSupplierDeliveryNote": "string",
  "invoiceDetailInvoiceSupplierId": 1,
  "invoiceDetailInvoiceSupplierInvoiceNo": "string",
  "invoiceDetailInvoiceSupplierName": "Ava Chen",
  "invoiceDetailInvoiceNoOfImages": 1,
  "invoiceDetailInvoiceTimestamp": 1,
  "invoiceDetailInvoiceType": 1,
  "invoiceDetailInvoiceUpdateSupplierOrAmount": true,
  "invoiceDetailInvoiceUseDiscount": true,
  "invoiceDetailInvoiceVatAmount": 1,
  "invoiceDetailInvoiceVat1Amount": 1,
  "invoiceDetailInvoiceVat2Amount": 1,
  "invoiceDetailInvoiceVat3Amount": 1,
  "invoiceDetailInvoiceVat4Amount": 1,
  "invoiceDetailInvoiceVatCalculation": true,
  "invoiceDetailInvoiceVatCode": "string",
  "invoiceDetailInvoiceVatCodeID": 1,
  "invoiceDetailInvoiceVatType": "string",
  "invoiceDetailInvoiceVatTypeId": 1,
  "invoiceDetailInvoiceVoucherNo": 1,
  "invoiceDetailInvoiceVoucherSeries": "string",
  "invoiceDetailInvoiceExternalId": "string",
  "invoiceDetailInvoiceExternalSource": "string",
  "invoiceDetailInvoiceIsDynamicFlow": true,
  "invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles": 1,
  "invoiceDetailInvoiceAuthorizationAmountData": {},
  "invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount": 1,
  "invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts": [
    "string"
  ],
  "invoiceDetailInvoiceAccountCodings": [
    "string"
  ],
  "invoiceDetailInvoiceFlows": [
    "string"
  ],
  "invoiceDetailInvoiceDiaries": [
    "string"
  ],
  "invoiceDetailObjectTypes": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/update-invoice-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceDetail": {},
    "invoiceDetailHeadersOnly": 1,
    "invoiceDetailForProcessing": true,
    "invoiceDetailLocked": true,
    "invoiceDetailLockedRowId": 1,
    "invoiceDetailLockedRowLoginName": "Ava Chen",
    "invoiceDetailLockedRowRole": "string",
    "invoiceDetailRowState": 1,
    "invoiceDetailSelected": true,
    "invoiceDetailKeyValuesRowState": 1,
    "invoiceDetailInvoice": {},
    "invoiceDetailInvoiceHeadersOnly": 1,
    "invoiceDetailInvoiceForProcessing": true,
    "invoiceDetailInvoiceLocked": true,
    "invoiceDetailInvoiceLockedRowId": 1,
    "invoiceDetailInvoiceLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceLockedRowRole": "string",
    "invoiceDetailInvoiceRowState": 1,
    "invoiceDetailInvoiceSelected": true,
    "invoiceDetailInvoiceKeyValuesRowState": 1,
    "invoiceDetailInvoiceAccount": "string",
    "invoiceDetailInvoiceAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAccountCodingProposal": "string",
    "invoiceDetailInvoiceAccountCodingProposalID": 1,
    "invoiceDetailInvoiceAccountId": 1,
    "invoiceDetailInvoiceAccountName": "Ava Chen",
    "invoiceDetailInvoiceAlternativeId": "string",
    "invoiceDetailInvoiceAmount": 1,
    "invoiceDetailInvoiceArrivalAccountCoded": true,
    "invoiceDetailInvoiceArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAsset": true,
    "invoiceDetailInvoiceAuthorizationRole": "string",
    "invoiceDetailInvoiceAuthorizationUser": "string",
    "invoiceDetailInvoiceBaseAmount": 1,
    "invoiceDetailInvoiceBaseCurrency": "string",
    "invoiceDetailInvoiceBaseNetAmount": 1,
    "invoiceDetailInvoiceBaseVatAmount": 1,
    "invoiceDetailInvoiceBlocked": true,
    "invoiceDetailInvoiceBuyingRate": 1,
    "invoiceDetailInvoiceChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceChUser": "string",
    "invoiceDetailInvoiceClassified": true,
    "invoiceDetailInvoiceCompany": "string",
    "invoiceDetailInvoiceCompanyDTO": {},
    "invoiceDetailInvoiceCompanyDTOHeadersOnly": 1,
    "invoiceDetailInvoiceCompanyDTOForProcessing": true,
    "invoiceDetailInvoiceCompanyDTOLocked": true,
    "invoiceDetailInvoiceCompanyDTOLockedRowId": 1,
    "invoiceDetailInvoiceCompanyDTOLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOLockedRowRole": "string",
    "invoiceDetailInvoiceCompanyDTORowState": 1,
    "invoiceDetailInvoiceCompanyDTOSelected": true,
    "invoiceDetailInvoiceCompanyDTOKeyValuesRowState": 1,
    "invoiceDetailInvoiceCompanyDTOCompany": "string",
    "invoiceDetailInvoiceCompanyDTOName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOType": "string",
    "invoiceDetailInvoiceCompanyDTOValidTo": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries": "string",
    "invoiceDetailInvoiceCompanyDTOBaseCurrency": "string",
    "invoiceDetailInvoiceCompanyDTOVatNo": "string",
    "invoiceDetailInvoiceCompanyDTOPostalAddressId": 1,
    "invoiceDetailInvoiceCompanyDTOWww": "string",
    "invoiceDetailInvoiceCompanyDTOContact": "string",
    "invoiceDetailInvoiceCompanyDTOEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOErrorHandlingRole": "string",
    "invoiceDetailInvoiceCompanyDTOCheckRange": 1,
    "invoiceDetailInvoiceCompanyDTOCheckCounter": 1,
    "invoiceDetailInvoiceCompanyDTOCheckRole": "string",
    "invoiceDetailInvoiceCompanyDTOCodeRelationIsActive": true,
    "invoiceDetailInvoiceCompanyDTOCodeRelationCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck": "string",
    "invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOArrivalType": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCoding": "string",
    "invoiceDetailInvoiceCompanyDTOAccountCodingDate": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateDueDate": "string",
    "invoiceDetailInvoiceCompanyDTOSetAccountCodedBy": true,
    "invoiceDetailInvoiceCompanyDTOFlowProposalId": 1,
    "invoiceDetailInvoiceCompanyDTOPaymentTermId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocationsAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOClassifySupplier": true,
    "invoiceDetailInvoiceCompanyDTODebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOCostAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat": true,
    "invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles": 1,
    "invoiceDetailInvoiceCompanyDTOSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign": true,
    "invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending": true,
    "invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit": 1,
    "invoiceDetailInvoiceCompanyDTOGetVatCodeFrom": "string",
    "invoiceDetailInvoiceCompanyDTOVatAccountCodingType": 1,
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo": 1,
    "invoiceDetailInvoiceCompanyDTOFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOUseReference": "string",
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAutoDelivery": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchPriceEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOErp": "string",
    "invoiceDetailInvoiceCompanyDTOGroup1": "string",
    "invoiceDetailInvoiceCompanyDTOGroup2": "string",
    "invoiceDetailInvoiceCompanyDTOGroup3": "string",
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign": true,
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder": true,
    "invoiceDetailInvoiceCompanyDTOChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOChUser": "string",
    "invoiceDetailInvoiceCompanyDTODirectRecording": true,
    "invoiceDetailInvoiceCompanyDTOVatExempt": true,
    "invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding": true,
    "invoiceDetailInvoiceCompanyDTOIdentifyBitCode": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseInstantReminder": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTORequisitionNoApproval": 1,
    "invoiceDetailInvoiceCompanyDTOEan": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount": true,
    "invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount": "string",
    "invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines": "string",
    "invoiceDetailInvoiceCompanyDTOUseBuyersHelp": true,
    "invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount": true,
    "invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit": true,
    "invoiceDetailInvoiceCompanyDTOObjectType1Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType2Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType3Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType4Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType5Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType6Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType7Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType8Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote": true,
    "invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote": true,
    "invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses": true,
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery": true,
    "invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired": true,
    "invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval": "string",
    "invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount": true,
    "invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTODeliveryCode": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting": "string",
    "invoiceDetailInvoiceCompanyDTOAllocationSetting": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine": true,
    "invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting": true,
    "invoiceDetailInvoiceCompanyDTOAiInvoice": "string",
    "invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate": true,
    "invoiceDetailInvoiceCompanyDTOSupplierMatchPattern": "string",
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2": 1,
    "invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns": true,
    "invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOVarianceVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOMaxVarianceAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAiNoPrediction": "string",
    "invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter": true,
    "invoiceDetailInvoiceCompanyDTOVat1AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat2AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat3AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat4AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult": "string",
    "invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTOContractNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTORillionCaptureUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTORillionCapturelabel": "string",
    "invoiceDetailInvoiceCompanyDTOEInvoiceUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTOEInvoiceLabel": "string",
    "invoiceDetailInvoiceCompanyDTOUseAmountInRounding": true,
    "invoiceDetailInvoiceCompanyDTORoundingAmount": 1,
    "invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting": 1,
    "invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod": true,
    "invoiceDetailInvoiceCompanyDTOCompanyAlias": ["string"],
    "invoiceDetailInvoiceCompanyName": "Ava Chen",
    "invoiceDetailInvoiceContractMatch": 1,
    "invoiceDetailInvoiceContractNo": "string",
    "invoiceDetailInvoiceCrDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCredit": true,
    "invoiceDetailInvoiceCreditTime": 1,
    "invoiceDetailInvoiceCurrency": "string",
    "invoiceDetailInvoiceCurrentLevel": 1,
    "invoiceDetailInvoiceCurrentRole": "string",
    "invoiceDetailInvoiceDeptAccountId": 1,
    "invoiceDetailInvoiceDiscountAmount": 1,
    "invoiceDetailInvoiceDiscountDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceDiscountGrossAmount": true,
    "invoiceDetailInvoiceDiscountPercentage": 1,
    "invoiceDetailInvoiceDueDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceEmailSignRole": "ava@example.com",
    "invoiceDetailInvoiceExchangeRate": 1,
    "invoiceDetailInvoiceSystemCurrencyExchangeRate": 1,
    "invoiceDetailInvoiceExpenseMatch": 1,
    "invoiceDetailInvoiceExtraAmount": 1,
    "invoiceDetailInvoiceExtraId": "string",
    "invoiceDetailInvoiceFeeAmount1": 1,
    "invoiceDetailInvoiceFeeAmount2": 1,
    "invoiceDetailInvoiceFeeAmount3": 1,
    "invoiceDetailInvoiceFileTypeId": 1,
    "invoiceDetailInvoiceFlowAddition": 1,
    "invoiceDetailInvoiceFlowProposal": "string",
    "invoiceDetailInvoiceFlowProposalId": 1,
    "invoiceDetailInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceForPartialPayment": true,
    "invoiceDetailInvoiceGroup1": "string",
    "invoiceDetailInvoiceGroup2": "string",
    "invoiceDetailInvoiceGroup3": "string",
    "invoiceDetailInvoiceGroup4": "string",
    "invoiceDetailInvoiceGroup5": "string",
    "invoiceDetailInvoiceGroup6": "string",
    "invoiceDetailInvoiceInvestigate": true,
    "invoiceDetailInvoiceInvoiceAccountCodingAmount": 1,
    "invoiceDetailInvoiceInvoiceDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceInvoiceFlowId": 1,
    "invoiceDetailInvoiceInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceInvoiceId": 1,
    "invoiceDetailInvoiceInvoiceImageFileExtension": "string",
    "invoiceDetailInvoiceInvoiceNo": 1,
    "invoiceDetailInvoiceInvoiceSeries": "string",
    "invoiceDetailInvoiceInvoiceStatusMessage": "string",
    "invoiceDetailInvoiceIsContractMatch": 1,
    "invoiceDetailInvoiceIsPurchaseOrderMatch": 1,
    "invoiceDetailInvoiceLatestDiaryNote": "string",
    "invoiceDetailInvoiceLatestDiaryNoteUser": "string",
    "invoiceDetailInvoiceLatestDiaryNoteTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceLinkedInvoiceId": 1,
    "invoiceDetailInvoiceLinkedInvoiceNo": 1,
    "invoiceDetailInvoiceLinkedInvoiceSeries": "https://example.com",
    "invoiceDetailInvoiceMatchedContractId": 1,
    "invoiceDetailInvoiceNetAmount": 1,
    "invoiceDetailInvoiceNoOfRoles": 1,
    "invoiceDetailInvoiceObject1": "string",
    "invoiceDetailInvoiceObject1Id": 1,
    "invoiceDetailInvoiceObject1Name": "Ava Chen",
    "invoiceDetailInvoiceObject2": "string",
    "invoiceDetailInvoiceObject2Id": 1,
    "invoiceDetailInvoiceObject2Name": "Ava Chen",
    "invoiceDetailInvoiceObject3": "string",
    "invoiceDetailInvoiceObject3Id": 1,
    "invoiceDetailInvoiceObject3Name": "Ava Chen",
    "invoiceDetailInvoiceObject4": "string",
    "invoiceDetailInvoiceObject4Id": 1,
    "invoiceDetailInvoiceObject4Name": "Ava Chen",
    "invoiceDetailInvoiceObject5": "string",
    "invoiceDetailInvoiceObject5Id": 1,
    "invoiceDetailInvoiceObject5Name": "Ava Chen",
    "invoiceDetailInvoiceObject6": "string",
    "invoiceDetailInvoiceObject6Id": 1,
    "invoiceDetailInvoiceObject6Name": "Ava Chen",
    "invoiceDetailInvoiceObject7": "string",
    "invoiceDetailInvoiceObject7Id": 1,
    "invoiceDetailInvoiceObject7Name": "Ava Chen",
    "invoiceDetailInvoiceObject8": "string",
    "invoiceDetailInvoiceObject8Id": 1,
    "invoiceDetailInvoiceObject8Name": "Ava Chen",
    "invoiceDetailInvoiceOldAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceOriginalSupplierId": 1,
    "invoiceDetailInvoiceOriginalSupplierName": "Ava Chen",
    "invoiceDetailInvoiceOriginalVatType": "string",
    "invoiceDetailInvoicePartialPaymentAmount": 1,
    "invoiceDetailInvoicePartialPaymentAmountUpdated": true,
    "invoiceDetailInvoicePaymentDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoicePaymentMessage": "string",
    "invoiceDetailInvoicePaymentTerm": "string",
    "invoiceDetailInvoicePaymentTermId": 1,
    "invoiceDetailInvoicePaymentTime": 1,
    "invoiceDetailInvoicePayReference": "string",
    "invoiceDetailInvoicePeriodAmount": 1,
    "invoiceDetailInvoicePostingsUpdated": true,
    "invoiceDetailInvoiceProcessDays": 1,
    "invoiceDetailInvoiceProcessTime": 1,
    "invoiceDetailInvoicePurchaseOrderMatch": 1,
    "invoiceDetailInvoicePurchaseOrderNo": "string",
    "invoiceDetailInvoiceReference1": "string",
    "invoiceDetailInvoiceReference2": "string",
    "invoiceDetailInvoiceRemainingPartialPaymentAmount": 1,
    "invoiceDetailInvoiceReminderReason": 1,
    "invoiceDetailInvoiceRole": "string",
    "invoiceDetailInvoiceShowDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceStatus": 1,
    "invoiceDetailInvoiceSupplier": "string",
    "invoiceDetailInvoiceSupplierActiveCreditCard": true,
    "invoiceDetailInvoiceSupplierAddress1": "string",
    "invoiceDetailInvoiceSupplierAddress2": "string",
    "invoiceDetailInvoiceSupplierAddress3": "string",
    "invoiceDetailInvoiceSupplierAddress4": "string",
    "invoiceDetailInvoiceSupplierAddress5": "string",
    "invoiceDetailInvoiceSupplierAddress6": "string",
    "invoiceDetailInvoiceSupplierBankAccount": "string",
    "invoiceDetailInvoiceSupplierDeliveryNote": "string",
    "invoiceDetailInvoiceSupplierId": 1,
    "invoiceDetailInvoiceSupplierInvoiceNo": "string",
    "invoiceDetailInvoiceSupplierName": "Ava Chen",
    "invoiceDetailInvoiceNoOfImages": 1,
    "invoiceDetailInvoiceTimestamp": 1,
    "invoiceDetailInvoiceType": 1,
    "invoiceDetailInvoiceUpdateSupplierOrAmount": true,
    "invoiceDetailInvoiceUseDiscount": true,
    "invoiceDetailInvoiceVatAmount": 1,
    "invoiceDetailInvoiceVat1Amount": 1,
    "invoiceDetailInvoiceVat2Amount": 1,
    "invoiceDetailInvoiceVat3Amount": 1,
    "invoiceDetailInvoiceVat4Amount": 1,
    "invoiceDetailInvoiceVatCalculation": true,
    "invoiceDetailInvoiceVatCode": "string",
    "invoiceDetailInvoiceVatCodeID": 1,
    "invoiceDetailInvoiceVatType": "string",
    "invoiceDetailInvoiceVatTypeId": 1,
    "invoiceDetailInvoiceVoucherNo": 1,
    "invoiceDetailInvoiceVoucherSeries": "string",
    "invoiceDetailInvoiceExternalId": "string",
    "invoiceDetailInvoiceExternalSource": "string",
    "invoiceDetailInvoiceIsDynamicFlow": true,
    "invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles": 1,
    "invoiceDetailInvoiceAuthorizationAmountData": {},
    "invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount": 1,
    "invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts": ["string"],
    "invoiceDetailInvoiceAccountCodings": ["string"],
    "invoiceDetailInvoiceFlows": ["string"],
    "invoiceDetailInvoiceDiaries": ["string"],
    "invoiceDetailObjectTypes": ["string"],
    "invoiceDetail": {},
    "invoiceDetailHeadersOnly": 1,
    "invoiceDetailForProcessing": true,
    "invoiceDetailLocked": true,
    "invoiceDetailLockedRowId": 1,
    "invoiceDetailLockedRowLoginName": "Ava Chen",
    "invoiceDetailLockedRowRole": "string",
    "invoiceDetailRowState": 1,
    "invoiceDetailSelected": true,
    "invoiceDetailKeyValuesRowState": 1,
    "invoiceDetailInvoice": {},
    "invoiceDetailInvoiceHeadersOnly": 1,
    "invoiceDetailInvoiceForProcessing": true,
    "invoiceDetailInvoiceLocked": true,
    "invoiceDetailInvoiceLockedRowId": 1,
    "invoiceDetailInvoiceLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceLockedRowRole": "string",
    "invoiceDetailInvoiceRowState": 1,
    "invoiceDetailInvoiceSelected": true,
    "invoiceDetailInvoiceKeyValuesRowState": 1,
    "invoiceDetailInvoiceAccount": "string",
    "invoiceDetailInvoiceAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAccountCodingProposal": "string",
    "invoiceDetailInvoiceAccountCodingProposalID": 1,
    "invoiceDetailInvoiceAccountId": 1,
    "invoiceDetailInvoiceAccountName": "Ava Chen",
    "invoiceDetailInvoiceAlternativeId": "string",
    "invoiceDetailInvoiceAmount": 1,
    "invoiceDetailInvoiceArrivalAccountCoded": true,
    "invoiceDetailInvoiceArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAsset": true,
    "invoiceDetailInvoiceAuthorizationRole": "string",
    "invoiceDetailInvoiceAuthorizationUser": "string",
    "invoiceDetailInvoiceBaseAmount": 1,
    "invoiceDetailInvoiceBaseCurrency": "string",
    "invoiceDetailInvoiceBaseNetAmount": 1,
    "invoiceDetailInvoiceBaseVatAmount": 1,
    "invoiceDetailInvoiceBlocked": true,
    "invoiceDetailInvoiceBuyingRate": 1,
    "invoiceDetailInvoiceChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceChUser": "string",
    "invoiceDetailInvoiceClassified": true,
    "invoiceDetailInvoiceCompany": "string",
    "invoiceDetailInvoiceCompanyDTO": {},
    "invoiceDetailInvoiceCompanyDTOHeadersOnly": 1,
    "invoiceDetailInvoiceCompanyDTOForProcessing": true,
    "invoiceDetailInvoiceCompanyDTOLocked": true,
    "invoiceDetailInvoiceCompanyDTOLockedRowId": 1,
    "invoiceDetailInvoiceCompanyDTOLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOLockedRowRole": "string",
    "invoiceDetailInvoiceCompanyDTORowState": 1,
    "invoiceDetailInvoiceCompanyDTOSelected": true,
    "invoiceDetailInvoiceCompanyDTOKeyValuesRowState": 1,
    "invoiceDetailInvoiceCompanyDTOCompany": "string",
    "invoiceDetailInvoiceCompanyDTOName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOType": "string",
    "invoiceDetailInvoiceCompanyDTOValidTo": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries": "string",
    "invoiceDetailInvoiceCompanyDTOBaseCurrency": "string",
    "invoiceDetailInvoiceCompanyDTOVatNo": "string",
    "invoiceDetailInvoiceCompanyDTOPostalAddressId": 1,
    "invoiceDetailInvoiceCompanyDTOWww": "string",
    "invoiceDetailInvoiceCompanyDTOContact": "string",
    "invoiceDetailInvoiceCompanyDTOEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOErrorHandlingRole": "string",
    "invoiceDetailInvoiceCompanyDTOCheckRange": 1,
    "invoiceDetailInvoiceCompanyDTOCheckCounter": 1,
    "invoiceDetailInvoiceCompanyDTOCheckRole": "string",
    "invoiceDetailInvoiceCompanyDTOCodeRelationIsActive": true,
    "invoiceDetailInvoiceCompanyDTOCodeRelationCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck": "string",
    "invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOArrivalType": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCoding": "string",
    "invoiceDetailInvoiceCompanyDTOAccountCodingDate": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateDueDate": "string",
    "invoiceDetailInvoiceCompanyDTOSetAccountCodedBy": true,
    "invoiceDetailInvoiceCompanyDTOFlowProposalId": 1,
    "invoiceDetailInvoiceCompanyDTOPaymentTermId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocationsAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOClassifySupplier": true,
    "invoiceDetailInvoiceCompanyDTODebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOCostAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat": true,
    "invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles": 1,
    "invoiceDetailInvoiceCompanyDTOSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign": true,
    "invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending": true,
    "invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit": 1,
    "invoiceDetailInvoiceCompanyDTOGetVatCodeFrom": "string",
    "invoiceDetailInvoiceCompanyDTOVatAccountCodingType": 1,
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo": 1,
    "invoiceDetailInvoiceCompanyDTOFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOUseReference": "string",
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAutoDelivery": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchPriceEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOErp": "string",
    "invoiceDetailInvoiceCompanyDTOGroup1": "string",
    "invoiceDetailInvoiceCompanyDTOGroup2": "string",
    "invoiceDetailInvoiceCompanyDTOGroup3": "string",
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign": true,
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder": true,
    "invoiceDetailInvoiceCompanyDTOChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOChUser": "string",
    "invoiceDetailInvoiceCompanyDTODirectRecording": true,
    "invoiceDetailInvoiceCompanyDTOVatExempt": true,
    "invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding": true,
    "invoiceDetailInvoiceCompanyDTOIdentifyBitCode": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseInstantReminder": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTORequisitionNoApproval": 1,
    "invoiceDetailInvoiceCompanyDTOEan": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount": true,
    "invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount": "string",
    "invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines": "string",
    "invoiceDetailInvoiceCompanyDTOUseBuyersHelp": true,
    "invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount": true,
    "invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit": true,
    "invoiceDetailInvoiceCompanyDTOObjectType1Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType2Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType3Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType4Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType5Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType6Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType7Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType8Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote": true,
    "invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote": true,
    "invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses": true,
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery": true,
    "invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired": true,
    "invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval": "string",
    "invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount": true,
    "invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTODeliveryCode": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting": "string",
    "invoiceDetailInvoiceCompanyDTOAllocationSetting": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine": true,
    "invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting": true,
    "invoiceDetailInvoiceCompanyDTOAiInvoice": "string",
    "invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate": true,
    "invoiceDetailInvoiceCompanyDTOSupplierMatchPattern": "string",
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2": 1,
    "invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns": true,
    "invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOVarianceVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOMaxVarianceAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAiNoPrediction": "string",
    "invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter": true,
    "invoiceDetailInvoiceCompanyDTOVat1AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat2AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat3AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat4AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult": "string",
    "invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTOContractNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTORillionCaptureUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTORillionCapturelabel": "string",
    "invoiceDetailInvoiceCompanyDTOEInvoiceUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTOEInvoiceLabel": "string",
    "invoiceDetailInvoiceCompanyDTOUseAmountInRounding": true,
    "invoiceDetailInvoiceCompanyDTORoundingAmount": 1,
    "invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting": 1,
    "invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod": true,
    "invoiceDetailInvoiceCompanyDTOCompanyAlias": ["string"],
    "invoiceDetailInvoiceCompanyName": "Ava Chen",
    "invoiceDetailInvoiceContractMatch": 1,
    "invoiceDetailInvoiceContractNo": "string",
    "invoiceDetailInvoiceCrDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCredit": true,
    "invoiceDetailInvoiceCreditTime": 1,
    "invoiceDetailInvoiceCurrency": "string",
    "invoiceDetailInvoiceCurrentLevel": 1,
    "invoiceDetailInvoiceCurrentRole": "string",
    "invoiceDetailInvoiceDeptAccountId": 1,
    "invoiceDetailInvoiceDiscountAmount": 1,
    "invoiceDetailInvoiceDiscountDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceDiscountGrossAmount": true,
    "invoiceDetailInvoiceDiscountPercentage": 1,
    "invoiceDetailInvoiceDueDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceEmailSignRole": "ava@example.com",
    "invoiceDetailInvoiceExchangeRate": 1,
    "invoiceDetailInvoiceSystemCurrencyExchangeRate": 1,
    "invoiceDetailInvoiceExpenseMatch": 1,
    "invoiceDetailInvoiceExtraAmount": 1,
    "invoiceDetailInvoiceExtraId": "string",
    "invoiceDetailInvoiceFeeAmount1": 1,
    "invoiceDetailInvoiceFeeAmount2": 1,
    "invoiceDetailInvoiceFeeAmount3": 1,
    "invoiceDetailInvoiceFileTypeId": 1,
    "invoiceDetailInvoiceFlowAddition": 1,
    "invoiceDetailInvoiceFlowProposal": "string",
    "invoiceDetailInvoiceFlowProposalId": 1,
    "invoiceDetailInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceForPartialPayment": true,
    "invoiceDetailInvoiceGroup1": "string",
    "invoiceDetailInvoiceGroup2": "string",
    "invoiceDetailInvoiceGroup3": "string",
    "invoiceDetailInvoiceGroup4": "string",
    "invoiceDetailInvoiceGroup5": "string",
    "invoiceDetailInvoiceGroup6": "string",
    "invoiceDetailInvoiceInvestigate": true,
    "invoiceDetailInvoiceInvoiceAccountCodingAmount": 1,
    "invoiceDetailInvoiceInvoiceDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceInvoiceFlowId": 1,
    "invoiceDetailInvoiceInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceInvoiceId": 1,
    "invoiceDetailInvoiceInvoiceImageFileExtension": "string",
    "invoiceDetailInvoiceInvoiceNo": 1,
    "invoiceDetailInvoiceInvoiceSeries": "string",
    "invoiceDetailInvoiceInvoiceStatusMessage": "string",
    "invoiceDetailInvoiceIsContractMatch": 1,
    "invoiceDetailInvoiceIsPurchaseOrderMatch": 1,
    "invoiceDetailInvoiceLatestDiaryNote": "string",
    "invoiceDetailInvoiceLatestDiaryNoteUser": "string",
    "invoiceDetailInvoiceLatestDiaryNoteTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceLinkedInvoiceId": 1,
    "invoiceDetailInvoiceLinkedInvoiceNo": 1,
    "invoiceDetailInvoiceLinkedInvoiceSeries": "https://example.com",
    "invoiceDetailInvoiceMatchedContractId": 1,
    "invoiceDetailInvoiceNetAmount": 1,
    "invoiceDetailInvoiceNoOfRoles": 1,
    "invoiceDetailInvoiceObject1": "string",
    "invoiceDetailInvoiceObject1Id": 1,
    "invoiceDetailInvoiceObject1Name": "Ava Chen",
    "invoiceDetailInvoiceObject2": "string",
    "invoiceDetailInvoiceObject2Id": 1,
    "invoiceDetailInvoiceObject2Name": "Ava Chen",
    "invoiceDetailInvoiceObject3": "string",
    "invoiceDetailInvoiceObject3Id": 1,
    "invoiceDetailInvoiceObject3Name": "Ava Chen",
    "invoiceDetailInvoiceObject4": "string",
    "invoiceDetailInvoiceObject4Id": 1,
    "invoiceDetailInvoiceObject4Name": "Ava Chen",
    "invoiceDetailInvoiceObject5": "string",
    "invoiceDetailInvoiceObject5Id": 1,
    "invoiceDetailInvoiceObject5Name": "Ava Chen",
    "invoiceDetailInvoiceObject6": "string",
    "invoiceDetailInvoiceObject6Id": 1,
    "invoiceDetailInvoiceObject6Name": "Ava Chen",
    "invoiceDetailInvoiceObject7": "string",
    "invoiceDetailInvoiceObject7Id": 1,
    "invoiceDetailInvoiceObject7Name": "Ava Chen",
    "invoiceDetailInvoiceObject8": "string",
    "invoiceDetailInvoiceObject8Id": 1,
    "invoiceDetailInvoiceObject8Name": "Ava Chen",
    "invoiceDetailInvoiceOldAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceOriginalSupplierId": 1,
    "invoiceDetailInvoiceOriginalSupplierName": "Ava Chen",
    "invoiceDetailInvoiceOriginalVatType": "string",
    "invoiceDetailInvoicePartialPaymentAmount": 1,
    "invoiceDetailInvoicePartialPaymentAmountUpdated": true,
    "invoiceDetailInvoicePaymentDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoicePaymentMessage": "string",
    "invoiceDetailInvoicePaymentTerm": "string",
    "invoiceDetailInvoicePaymentTermId": 1,
    "invoiceDetailInvoicePaymentTime": 1,
    "invoiceDetailInvoicePayReference": "string",
    "invoiceDetailInvoicePeriodAmount": 1,
    "invoiceDetailInvoicePostingsUpdated": true,
    "invoiceDetailInvoiceProcessDays": 1,
    "invoiceDetailInvoiceProcessTime": 1,
    "invoiceDetailInvoicePurchaseOrderMatch": 1,
    "invoiceDetailInvoicePurchaseOrderNo": "string",
    "invoiceDetailInvoiceReference1": "string",
    "invoiceDetailInvoiceReference2": "string",
    "invoiceDetailInvoiceRemainingPartialPaymentAmount": 1,
    "invoiceDetailInvoiceReminderReason": 1,
    "invoiceDetailInvoiceRole": "string",
    "invoiceDetailInvoiceShowDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceStatus": 1,
    "invoiceDetailInvoiceSupplier": "string",
    "invoiceDetailInvoiceSupplierActiveCreditCard": true,
    "invoiceDetailInvoiceSupplierAddress1": "string",
    "invoiceDetailInvoiceSupplierAddress2": "string",
    "invoiceDetailInvoiceSupplierAddress3": "string",
    "invoiceDetailInvoiceSupplierAddress4": "string",
    "invoiceDetailInvoiceSupplierAddress5": "string",
    "invoiceDetailInvoiceSupplierAddress6": "string",
    "invoiceDetailInvoiceSupplierBankAccount": "string",
    "invoiceDetailInvoiceSupplierDeliveryNote": "string",
    "invoiceDetailInvoiceSupplierId": 1,
    "invoiceDetailInvoiceSupplierInvoiceNo": "string",
    "invoiceDetailInvoiceSupplierName": "Ava Chen",
    "invoiceDetailInvoiceNoOfImages": 1,
    "invoiceDetailInvoiceTimestamp": 1,
    "invoiceDetailInvoiceType": 1,
    "invoiceDetailInvoiceUpdateSupplierOrAmount": true,
    "invoiceDetailInvoiceUseDiscount": true,
    "invoiceDetailInvoiceVatAmount": 1,
    "invoiceDetailInvoiceVat1Amount": 1,
    "invoiceDetailInvoiceVat2Amount": 1,
    "invoiceDetailInvoiceVat3Amount": 1,
    "invoiceDetailInvoiceVat4Amount": 1,
    "invoiceDetailInvoiceVatCalculation": true,
    "invoiceDetailInvoiceVatCode": "string",
    "invoiceDetailInvoiceVatCodeID": 1,
    "invoiceDetailInvoiceVatType": "string",
    "invoiceDetailInvoiceVatTypeId": 1,
    "invoiceDetailInvoiceVoucherNo": 1,
    "invoiceDetailInvoiceVoucherSeries": "string",
    "invoiceDetailInvoiceExternalId": "string",
    "invoiceDetailInvoiceExternalSource": "string",
    "invoiceDetailInvoiceIsDynamicFlow": true,
    "invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles": 1,
    "invoiceDetailInvoiceAuthorizationAmountData": {},
    "invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount": 1,
    "invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts": ["string"],
    "invoiceDetailInvoiceAccountCodings": ["string"],
    "invoiceDetailInvoiceFlows": ["string"],
    "invoiceDetailInvoiceDiaries": ["string"],
    "invoiceDetailObjectTypes": ["string"],
    "invoiceDetail": {},
    "invoiceDetailHeadersOnly": 1,
    "invoiceDetailForProcessing": true,
    "invoiceDetailLocked": true,
    "invoiceDetailLockedRowId": 1,
    "invoiceDetailLockedRowLoginName": "Ava Chen",
    "invoiceDetailLockedRowRole": "string",
    "invoiceDetailRowState": 1,
    "invoiceDetailSelected": true,
    "invoiceDetailKeyValuesRowState": 1,
    "invoiceDetailInvoice": {},
    "invoiceDetailInvoiceHeadersOnly": 1,
    "invoiceDetailInvoiceForProcessing": true,
    "invoiceDetailInvoiceLocked": true,
    "invoiceDetailInvoiceLockedRowId": 1,
    "invoiceDetailInvoiceLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceLockedRowRole": "string",
    "invoiceDetailInvoiceRowState": 1,
    "invoiceDetailInvoiceSelected": true,
    "invoiceDetailInvoiceKeyValuesRowState": 1,
    "invoiceDetailInvoiceAccount": "string",
    "invoiceDetailInvoiceAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAccountCodingProposal": "string",
    "invoiceDetailInvoiceAccountCodingProposalID": 1,
    "invoiceDetailInvoiceAccountId": 1,
    "invoiceDetailInvoiceAccountName": "Ava Chen",
    "invoiceDetailInvoiceAlternativeId": "string",
    "invoiceDetailInvoiceAmount": 1,
    "invoiceDetailInvoiceArrivalAccountCoded": true,
    "invoiceDetailInvoiceArrivalAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceArrivalTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceAsset": true,
    "invoiceDetailInvoiceAuthorizationRole": "string",
    "invoiceDetailInvoiceAuthorizationUser": "string",
    "invoiceDetailInvoiceBaseAmount": 1,
    "invoiceDetailInvoiceBaseCurrency": "string",
    "invoiceDetailInvoiceBaseNetAmount": 1,
    "invoiceDetailInvoiceBaseVatAmount": 1,
    "invoiceDetailInvoiceBlocked": true,
    "invoiceDetailInvoiceBuyingRate": 1,
    "invoiceDetailInvoiceChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceChUser": "string",
    "invoiceDetailInvoiceClassified": true,
    "invoiceDetailInvoiceCompany": "string",
    "invoiceDetailInvoiceCompanyDTO": {},
    "invoiceDetailInvoiceCompanyDTOHeadersOnly": 1,
    "invoiceDetailInvoiceCompanyDTOForProcessing": true,
    "invoiceDetailInvoiceCompanyDTOLocked": true,
    "invoiceDetailInvoiceCompanyDTOLockedRowId": 1,
    "invoiceDetailInvoiceCompanyDTOLockedRowLoginName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOLockedRowRole": "string",
    "invoiceDetailInvoiceCompanyDTORowState": 1,
    "invoiceDetailInvoiceCompanyDTOSelected": true,
    "invoiceDetailInvoiceCompanyDTOKeyValuesRowState": 1,
    "invoiceDetailInvoiceCompanyDTOCompany": "string",
    "invoiceDetailInvoiceCompanyDTOName": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOType": "string",
    "invoiceDetailInvoiceCompanyDTOValidTo": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries": "string",
    "invoiceDetailInvoiceCompanyDTOBaseCurrency": "string",
    "invoiceDetailInvoiceCompanyDTOVatNo": "string",
    "invoiceDetailInvoiceCompanyDTOPostalAddressId": 1,
    "invoiceDetailInvoiceCompanyDTOWww": "string",
    "invoiceDetailInvoiceCompanyDTOContact": "string",
    "invoiceDetailInvoiceCompanyDTOEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOErrorHandlingRole": "string",
    "invoiceDetailInvoiceCompanyDTOCheckRange": 1,
    "invoiceDetailInvoiceCompanyDTOCheckCounter": 1,
    "invoiceDetailInvoiceCompanyDTOCheckRole": "string",
    "invoiceDetailInvoiceCompanyDTOCodeRelationIsActive": true,
    "invoiceDetailInvoiceCompanyDTOCodeRelationCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck": "string",
    "invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck": true,
    "invoiceDetailInvoiceCompanyDTOArrivalType": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCoding": "string",
    "invoiceDetailInvoiceCompanyDTOAccountCodingDate": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateDueDate": "string",
    "invoiceDetailInvoiceCompanyDTOSetAccountCodedBy": true,
    "invoiceDetailInvoiceCompanyDTOFlowProposalId": 1,
    "invoiceDetailInvoiceCompanyDTOPaymentTermId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocationsAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOClassifySupplier": true,
    "invoiceDetailInvoiceCompanyDTODebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOCostAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat": true,
    "invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles": 1,
    "invoiceDetailInvoiceCompanyDTOSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign": true,
    "invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending": true,
    "invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit": 1,
    "invoiceDetailInvoiceCompanyDTOGetVatCodeFrom": "string",
    "invoiceDetailInvoiceCompanyDTOVatAccountCodingType": 1,
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo": 1,
    "invoiceDetailInvoiceCompanyDTOFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOUseReference": "string",
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAutoDelivery": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays": 1,
    "invoiceDetailInvoiceCompanyDTOReMatchPriceEmail": "ava@example.com",
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount1": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount2": 1,
    "invoiceDetailInvoiceCompanyDTOMaxFeeAmount3": 1,
    "invoiceDetailInvoiceCompanyDTOErp": "string",
    "invoiceDetailInvoiceCompanyDTOGroup1": "string",
    "invoiceDetailInvoiceCompanyDTOGroup2": "string",
    "invoiceDetailInvoiceCompanyDTOGroup3": "string",
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign": true,
    "invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder": true,
    "invoiceDetailInvoiceCompanyDTOChTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCompanyDTOChUser": "string",
    "invoiceDetailInvoiceCompanyDTODirectRecording": true,
    "invoiceDetailInvoiceCompanyDTOVatExempt": true,
    "invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding": true,
    "invoiceDetailInvoiceCompanyDTOIdentifyBitCode": 1,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier": true,
    "invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder": "string",
    "invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder": 1,
    "invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseInstantReminder": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId": 1,
    "invoiceDetailInvoiceCompanyDTOExpenseSigningRule": "string",
    "invoiceDetailInvoiceCompanyDTORequisitionNoApproval": 1,
    "invoiceDetailInvoiceCompanyDTOEan": "string",
    "invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount": true,
    "invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount": "string",
    "invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines": "string",
    "invoiceDetailInvoiceCompanyDTOUseBuyersHelp": true,
    "invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount": true,
    "invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit": true,
    "invoiceDetailInvoiceCompanyDTOObjectType1Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType2Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType3Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType4Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType5Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType6Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType7Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOObjectType8Name": "Ava Chen",
    "invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote": true,
    "invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote": true,
    "invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses": true,
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown": "string",
    "invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown": 1,
    "invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery": true,
    "invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired": true,
    "invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval": "string",
    "invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount": true,
    "invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval": true,
    "invoiceDetailInvoiceCompanyDTODeliveryCode": "string",
    "invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting": "string",
    "invoiceDetailInvoiceCompanyDTOAllocationSetting": "string",
    "invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine": true,
    "invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting": "string",
    "invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting": true,
    "invoiceDetailInvoiceCompanyDTOAiInvoice": "string",
    "invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer": "string",
    "invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate": true,
    "invoiceDetailInvoiceCompanyDTOSupplierMatchPattern": "string",
    "invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2": 1,
    "invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns": true,
    "invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType": "string",
    "invoiceDetailInvoiceCompanyDTOVarianceVatAccountId": 1,
    "invoiceDetailInvoiceCompanyDTOMaxVarianceAmount": 1,
    "invoiceDetailInvoiceCompanyDTOAiNoPrediction": "string",
    "invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter": true,
    "invoiceDetailInvoiceCompanyDTOVat1AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat2AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat3AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOVat4AccountId": 1,
    "invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult": "string",
    "invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching": true,
    "invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTOContractNoregexValidation": "string",
    "invoiceDetailInvoiceCompanyDTORillionCaptureUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTORillionCapturelabel": "string",
    "invoiceDetailInvoiceCompanyDTOEInvoiceUrl": "https://example.com",
    "invoiceDetailInvoiceCompanyDTOEInvoiceLabel": "string",
    "invoiceDetailInvoiceCompanyDTOUseAmountInRounding": true,
    "invoiceDetailInvoiceCompanyDTORoundingAmount": 1,
    "invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate": true,
    "invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting": 1,
    "invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod": true,
    "invoiceDetailInvoiceCompanyDTOCompanyAlias": ["string"],
    "invoiceDetailInvoiceCompanyName": "Ava Chen",
    "invoiceDetailInvoiceContractMatch": 1,
    "invoiceDetailInvoiceContractNo": "string",
    "invoiceDetailInvoiceCrDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceCredit": true,
    "invoiceDetailInvoiceCreditTime": 1,
    "invoiceDetailInvoiceCurrency": "string",
    "invoiceDetailInvoiceCurrentLevel": 1,
    "invoiceDetailInvoiceCurrentRole": "string",
    "invoiceDetailInvoiceDeptAccountId": 1,
    "invoiceDetailInvoiceDiscountAmount": 1,
    "invoiceDetailInvoiceDiscountDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceDiscountGrossAmount": true,
    "invoiceDetailInvoiceDiscountPercentage": 1,
    "invoiceDetailInvoiceDueDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceEmailSignRole": "ava@example.com",
    "invoiceDetailInvoiceExchangeRate": 1,
    "invoiceDetailInvoiceSystemCurrencyExchangeRate": 1,
    "invoiceDetailInvoiceExpenseMatch": 1,
    "invoiceDetailInvoiceExtraAmount": 1,
    "invoiceDetailInvoiceExtraId": "string",
    "invoiceDetailInvoiceFeeAmount1": 1,
    "invoiceDetailInvoiceFeeAmount2": 1,
    "invoiceDetailInvoiceFeeAmount3": 1,
    "invoiceDetailInvoiceFileTypeId": 1,
    "invoiceDetailInvoiceFlowAddition": 1,
    "invoiceDetailInvoiceFlowProposal": "string",
    "invoiceDetailInvoiceFlowProposalId": 1,
    "invoiceDetailInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceForPartialPayment": true,
    "invoiceDetailInvoiceGroup1": "string",
    "invoiceDetailInvoiceGroup2": "string",
    "invoiceDetailInvoiceGroup3": "string",
    "invoiceDetailInvoiceGroup4": "string",
    "invoiceDetailInvoiceGroup5": "string",
    "invoiceDetailInvoiceGroup6": "string",
    "invoiceDetailInvoiceInvestigate": true,
    "invoiceDetailInvoiceInvoiceAccountCodingAmount": 1,
    "invoiceDetailInvoiceInvoiceDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceInvoiceFlowId": 1,
    "invoiceDetailInvoiceInvoiceFlowStatus": 1,
    "invoiceDetailInvoiceInvoiceId": 1,
    "invoiceDetailInvoiceInvoiceImageFileExtension": "string",
    "invoiceDetailInvoiceInvoiceNo": 1,
    "invoiceDetailInvoiceInvoiceSeries": "string",
    "invoiceDetailInvoiceInvoiceStatusMessage": "string",
    "invoiceDetailInvoiceIsContractMatch": 1,
    "invoiceDetailInvoiceIsPurchaseOrderMatch": 1,
    "invoiceDetailInvoiceLatestDiaryNote": "string",
    "invoiceDetailInvoiceLatestDiaryNoteUser": "string",
    "invoiceDetailInvoiceLatestDiaryNoteTime": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceLinkedInvoiceId": 1,
    "invoiceDetailInvoiceLinkedInvoiceNo": 1,
    "invoiceDetailInvoiceLinkedInvoiceSeries": "https://example.com",
    "invoiceDetailInvoiceMatchedContractId": 1,
    "invoiceDetailInvoiceNetAmount": 1,
    "invoiceDetailInvoiceNoOfRoles": 1,
    "invoiceDetailInvoiceObject1": "string",
    "invoiceDetailInvoiceObject1Id": 1,
    "invoiceDetailInvoiceObject1Name": "Ava Chen",
    "invoiceDetailInvoiceObject2": "string",
    "invoiceDetailInvoiceObject2Id": 1,
    "invoiceDetailInvoiceObject2Name": "Ava Chen",
    "invoiceDetailInvoiceObject3": "string",
    "invoiceDetailInvoiceObject3Id": 1,
    "invoiceDetailInvoiceObject3Name": "Ava Chen",
    "invoiceDetailInvoiceObject4": "string",
    "invoiceDetailInvoiceObject4Id": 1,
    "invoiceDetailInvoiceObject4Name": "Ava Chen",
    "invoiceDetailInvoiceObject5": "string",
    "invoiceDetailInvoiceObject5Id": 1,
    "invoiceDetailInvoiceObject5Name": "Ava Chen",
    "invoiceDetailInvoiceObject6": "string",
    "invoiceDetailInvoiceObject6Id": 1,
    "invoiceDetailInvoiceObject6Name": "Ava Chen",
    "invoiceDetailInvoiceObject7": "string",
    "invoiceDetailInvoiceObject7Id": 1,
    "invoiceDetailInvoiceObject7Name": "Ava Chen",
    "invoiceDetailInvoiceObject8": "string",
    "invoiceDetailInvoiceObject8Id": 1,
    "invoiceDetailInvoiceObject8Name": "Ava Chen",
    "invoiceDetailInvoiceOldAccountCodingDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceOriginalSupplierId": 1,
    "invoiceDetailInvoiceOriginalSupplierName": "Ava Chen",
    "invoiceDetailInvoiceOriginalVatType": "string",
    "invoiceDetailInvoicePartialPaymentAmount": 1,
    "invoiceDetailInvoicePartialPaymentAmountUpdated": true,
    "invoiceDetailInvoicePaymentDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoicePaymentMessage": "string",
    "invoiceDetailInvoicePaymentTerm": "string",
    "invoiceDetailInvoicePaymentTermId": 1,
    "invoiceDetailInvoicePaymentTime": 1,
    "invoiceDetailInvoicePayReference": "string",
    "invoiceDetailInvoicePeriodAmount": 1,
    "invoiceDetailInvoicePostingsUpdated": true,
    "invoiceDetailInvoiceProcessDays": 1,
    "invoiceDetailInvoiceProcessTime": 1,
    "invoiceDetailInvoicePurchaseOrderMatch": 1,
    "invoiceDetailInvoicePurchaseOrderNo": "string",
    "invoiceDetailInvoiceReference1": "string",
    "invoiceDetailInvoiceReference2": "string",
    "invoiceDetailInvoiceRemainingPartialPaymentAmount": 1,
    "invoiceDetailInvoiceReminderReason": 1,
    "invoiceDetailInvoiceRole": "string",
    "invoiceDetailInvoiceShowDate": "2026-05-07T12:00:00.000Z",
    "invoiceDetailInvoiceStatus": 1,
    "invoiceDetailInvoiceSupplier": "string",
    "invoiceDetailInvoiceSupplierActiveCreditCard": true,
    "invoiceDetailInvoiceSupplierAddress1": "string",
    "invoiceDetailInvoiceSupplierAddress2": "string",
    "invoiceDetailInvoiceSupplierAddress3": "string",
    "invoiceDetailInvoiceSupplierAddress4": "string",
    "invoiceDetailInvoiceSupplierAddress5": "string",
    "invoiceDetailInvoiceSupplierAddress6": "string",
    "invoiceDetailInvoiceSupplierBankAccount": "string",
    "invoiceDetailInvoiceSupplierDeliveryNote": "string",
    "invoiceDetailInvoiceSupplierId": 1,
    "invoiceDetailInvoiceSupplierInvoiceNo": "string",
    "invoiceDetailInvoiceSupplierName": "Ava Chen",
    "invoiceDetailInvoiceNoOfImages": 1,
    "invoiceDetailInvoiceTimestamp": 1,
    "invoiceDetailInvoiceType": 1,
    "invoiceDetailInvoiceUpdateSupplierOrAmount": true,
    "invoiceDetailInvoiceUseDiscount": true,
    "invoiceDetailInvoiceVatAmount": 1,
    "invoiceDetailInvoiceVat1Amount": 1,
    "invoiceDetailInvoiceVat2Amount": 1,
    "invoiceDetailInvoiceVat3Amount": 1,
    "invoiceDetailInvoiceVat4Amount": 1,
    "invoiceDetailInvoiceVatCalculation": true,
    "invoiceDetailInvoiceVatCode": "string",
    "invoiceDetailInvoiceVatCodeID": 1,
    "invoiceDetailInvoiceVatType": "string",
    "invoiceDetailInvoiceVatTypeId": 1,
    "invoiceDetailInvoiceVoucherNo": 1,
    "invoiceDetailInvoiceVoucherSeries": "string",
    "invoiceDetailInvoiceExternalId": "string",
    "invoiceDetailInvoiceExternalSource": "string",
    "invoiceDetailInvoiceIsDynamicFlow": true,
    "invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles": 1,
    "invoiceDetailInvoiceAuthorizationAmountData": {},
    "invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount": 1,
    "invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts": ["string"],
    "invoiceDetailInvoiceAccountCodings": ["string"],
    "invoiceDetailInvoiceFlows": ["string"],
    "invoiceDetailInvoiceDiaries": ["string"],
    "invoiceDetailObjectTypes": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `role` | string | no | Optional query value for Role. Example: `Administrator`. |
| `invoiceDetail` | object | yes | Request body value for InvoiceDetail. |
| `invoiceDetailHeadersOnly` | number | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetailForProcessing` | boolean | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetailLocked` | boolean | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetailLockedRowId` | number | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetailLockedRowLoginName` | string | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetailLockedRowRole` | string | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetailRowState` | number | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetailSelected` | boolean | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetailKeyValuesRowState` | number | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetailInvoice` | object | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetailInvoiceHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetailInvoiceForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetailInvoiceLocked` | boolean | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetailInvoiceLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetailInvoiceLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetailInvoiceLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetailInvoiceRowState` | number | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetailInvoiceSelected` | boolean | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetailInvoiceKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetailInvoiceAccount` | string | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetailInvoiceAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetailInvoiceAccountCodingProposal` | string | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetailInvoiceAccountCodingProposalID` | number | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetailInvoiceAccountId` | number | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetailInvoiceAccountName` | string | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetailInvoiceAlternativeId` | string | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetailInvoiceAmount` | number | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetailInvoiceArrivalAccountCoded` | boolean | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetailInvoiceArrivalAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetailInvoiceArrivalDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetailInvoiceArrivalTime` | date | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetailInvoiceAsset` | boolean | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetailInvoiceAuthorizationRole` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetailInvoiceAuthorizationUser` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetailInvoiceBaseAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetailInvoiceBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetailInvoiceBaseNetAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetailInvoiceBaseVatAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetailInvoiceBlocked` | boolean | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetailInvoiceBuyingRate` | number | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetailInvoiceChTime` | date | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetailInvoiceChUser` | string | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetailInvoiceClassified` | boolean | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetailInvoiceCompany` | string | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetailInvoiceCompanyDTO` | object | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetailInvoiceCompanyDTOHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetailInvoiceCompanyDTOForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetailInvoiceCompanyDTOLocked` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetailInvoiceCompanyDTOLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetailInvoiceCompanyDTOLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetailInvoiceCompanyDTOLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetailInvoiceCompanyDTORowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetailInvoiceCompanyDTOSelected` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetailInvoiceCompanyDTOKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetailInvoiceCompanyDTOCompany` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetailInvoiceCompanyDTOName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetailInvoiceCompanyDTOType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetailInvoiceCompanyDTOValidTo` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetailInvoiceCompanyDTOInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetailInvoiceCompanyDTOBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetailInvoiceCompanyDTOVatNo` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetailInvoiceCompanyDTOPostalAddressId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetailInvoiceCompanyDTOWww` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetailInvoiceCompanyDTOContact` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetailInvoiceCompanyDTOEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetailInvoiceCompanyDTOErrorHandlingRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetailInvoiceCompanyDTOCheckRange` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetailInvoiceCompanyDTOCheckCounter` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetailInvoiceCompanyDTOCheckRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationIsActive` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOArrivalType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCoding` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetailInvoiceCompanyDTOAccountCodingDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetailInvoiceCompanyDTOCalculateDueDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetailInvoiceCompanyDTOSetAccountCodedBy` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetailInvoiceCompanyDTOPaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetailInvoiceCompanyDTOClassifySupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetailInvoiceCompanyDTODebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOCostAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetailInvoiceCompanyDTOVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetailInvoiceCompanyDTOSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetailInvoiceCompanyDTOGetVatCodeFrom` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetailInvoiceCompanyDTOVatAccountCodingType` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetailInvoiceCompanyDTOFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOUseReference` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAutoDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOErp` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetailInvoiceCompanyDTOGroup1` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetailInvoiceCompanyDTOGroup2` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetailInvoiceCompanyDTOGroup3` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOChTime` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetailInvoiceCompanyDTOChUser` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetailInvoiceCompanyDTODirectRecording` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetailInvoiceCompanyDTOVatExempt` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetailInvoiceCompanyDTOIdentifyBitCode` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetailInvoiceCompanyDTOExpenseInstantReminder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetailInvoiceCompanyDTOExpenseSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetailInvoiceCompanyDTORequisitionNoApproval` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetailInvoiceCompanyDTOEan` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetailInvoiceCompanyDTOUseBuyersHelp` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetailInvoiceCompanyDTOObjectType1Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType2Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType3Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType4Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType5Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType6Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType7Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType8Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTODeliveryCode` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetailInvoiceCompanyDTOAllocationSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetailInvoiceCompanyDTOAiInvoice` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetailInvoiceCompanyDTOSupplierMatchPattern` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetailInvoiceCompanyDTOVarianceVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetailInvoiceCompanyDTOMaxVarianceAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetailInvoiceCompanyDTOAiNoPrediction` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetailInvoiceCompanyDTOVat1AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat2AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat3AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat4AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTOContractNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTORillionCaptureUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetailInvoiceCompanyDTORillionCapturelabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceLabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetailInvoiceCompanyDTOUseAmountInRounding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetailInvoiceCompanyDTORoundingAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetailInvoiceCompanyDTOCompanyAlias` | array | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetailInvoiceCompanyName` | string | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetailInvoiceContractMatch` | number | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetailInvoiceContractNo` | string | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetailInvoiceCrDate` | date | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetailInvoiceCredit` | boolean | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetailInvoiceCreditTime` | number | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetailInvoiceCurrency` | string | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetailInvoiceCurrentLevel` | number | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetailInvoiceCurrentRole` | string | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetailInvoiceDeptAccountId` | number | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetailInvoiceDiscountAmount` | number | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetailInvoiceDiscountDate` | date | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetailInvoiceDiscountGrossAmount` | boolean | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetailInvoiceDiscountPercentage` | number | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetailInvoiceDueDate` | date | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetailInvoiceEmailSignRole` | string | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetailInvoiceExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetailInvoiceSystemCurrencyExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetailInvoiceExpenseMatch` | number | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetailInvoiceExtraAmount` | number | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetailInvoiceExtraId` | string | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetailInvoiceFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetailInvoiceFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetailInvoiceFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetailInvoiceFileTypeId` | number | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetailInvoiceFlowAddition` | number | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetailInvoiceFlowProposal` | string | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetailInvoiceFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetailInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetailInvoiceForPartialPayment` | boolean | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetailInvoiceGroup1` | string | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetailInvoiceGroup2` | string | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetailInvoiceGroup3` | string | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetailInvoiceGroup4` | string | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetailInvoiceGroup5` | string | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetailInvoiceGroup6` | string | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetailInvoiceInvestigate` | boolean | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetailInvoiceInvoiceAccountCodingAmount` | number | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetailInvoiceInvoiceDate` | date | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetailInvoiceInvoiceFlowId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetailInvoiceInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetailInvoiceInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetailInvoiceInvoiceImageFileExtension` | string | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetailInvoiceInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetailInvoiceInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetailInvoiceInvoiceStatusMessage` | string | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetailInvoiceIsContractMatch` | number | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetailInvoiceIsPurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetailInvoiceLatestDiaryNote` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetailInvoiceLatestDiaryNoteUser` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetailInvoiceLatestDiaryNoteTime` | date | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetailInvoiceLinkedInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetailInvoiceLinkedInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetailInvoiceLinkedInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetailInvoiceMatchedContractId` | number | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetailInvoiceNetAmount` | number | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetailInvoiceNoOfRoles` | number | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetailInvoiceObject1` | string | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetailInvoiceObject1Id` | number | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetailInvoiceObject1Name` | string | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetailInvoiceObject2` | string | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetailInvoiceObject2Id` | number | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetailInvoiceObject2Name` | string | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetailInvoiceObject3` | string | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetailInvoiceObject3Id` | number | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetailInvoiceObject3Name` | string | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetailInvoiceObject4` | string | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetailInvoiceObject4Id` | number | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetailInvoiceObject4Name` | string | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetailInvoiceObject5` | string | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetailInvoiceObject5Id` | number | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetailInvoiceObject5Name` | string | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetailInvoiceObject6` | string | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetailInvoiceObject6Id` | number | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetailInvoiceObject6Name` | string | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetailInvoiceObject7` | string | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetailInvoiceObject7Id` | number | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetailInvoiceObject7Name` | string | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetailInvoiceObject8` | string | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetailInvoiceObject8Id` | number | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetailInvoiceObject8Name` | string | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetailInvoiceOldAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetailInvoiceOriginalSupplierId` | number | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetailInvoiceOriginalSupplierName` | string | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetailInvoiceOriginalVatType` | string | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetailInvoicePartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetailInvoicePartialPaymentAmountUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetailInvoicePaymentDate` | date | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetailInvoicePaymentMessage` | string | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetailInvoicePaymentTerm` | string | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetailInvoicePaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetailInvoicePaymentTime` | number | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetailInvoicePayReference` | string | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetailInvoicePeriodAmount` | number | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetailInvoicePostingsUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetailInvoiceProcessDays` | number | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetailInvoiceProcessTime` | number | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetailInvoicePurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetailInvoicePurchaseOrderNo` | string | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetailInvoiceReference1` | string | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetailInvoiceReference2` | string | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetailInvoiceRemainingPartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetailInvoiceReminderReason` | number | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetailInvoiceRole` | string | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetailInvoiceShowDate` | date | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetailInvoiceStatus` | number | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetailInvoiceSupplier` | string | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetailInvoiceSupplierActiveCreditCard` | boolean | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetailInvoiceSupplierAddress1` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetailInvoiceSupplierAddress2` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetailInvoiceSupplierAddress3` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetailInvoiceSupplierAddress4` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetailInvoiceSupplierAddress5` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetailInvoiceSupplierAddress6` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetailInvoiceSupplierBankAccount` | string | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetailInvoiceSupplierDeliveryNote` | string | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetailInvoiceSupplierId` | number | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetailInvoiceSupplierInvoiceNo` | string | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetailInvoiceSupplierName` | string | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetailInvoiceNoOfImages` | number | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetailInvoiceTimestamp` | number | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetailInvoiceType` | number | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetailInvoiceUpdateSupplierOrAmount` | boolean | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetailInvoiceUseDiscount` | boolean | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetailInvoiceVatAmount` | number | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetailInvoiceVat1Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetailInvoiceVat2Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetailInvoiceVat3Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetailInvoiceVat4Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetailInvoiceVatCalculation` | boolean | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetailInvoiceVatCode` | string | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetailInvoiceVatCodeID` | number | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetailInvoiceVatType` | string | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetailInvoiceVatTypeId` | number | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetailInvoiceVoucherNo` | number | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetailInvoiceVoucherSeries` | string | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetailInvoiceExternalId` | string | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetailInvoiceExternalSource` | string | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetailInvoiceIsDynamicFlow` | boolean | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetailInvoiceAuthorizationAmountData` | object | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts` | array | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetailInvoiceAccountCodings` | array | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetailInvoiceFlows` | array | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetailInvoiceDiaries` | array | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetailObjectTypes` | array | yes | Request body value for InvoiceDetail ObjectTypes. |
| `invoiceDetail` | object | yes | Request body value for InvoiceDetail. |
| `invoiceDetailHeadersOnly` | number | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetailForProcessing` | boolean | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetailLocked` | boolean | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetailLockedRowId` | number | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetailLockedRowLoginName` | string | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetailLockedRowRole` | string | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetailRowState` | number | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetailSelected` | boolean | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetailKeyValuesRowState` | number | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetailInvoice` | object | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetailInvoiceHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetailInvoiceForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetailInvoiceLocked` | boolean | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetailInvoiceLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetailInvoiceLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetailInvoiceLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetailInvoiceRowState` | number | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetailInvoiceSelected` | boolean | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetailInvoiceKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetailInvoiceAccount` | string | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetailInvoiceAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetailInvoiceAccountCodingProposal` | string | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetailInvoiceAccountCodingProposalID` | number | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetailInvoiceAccountId` | number | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetailInvoiceAccountName` | string | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetailInvoiceAlternativeId` | string | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetailInvoiceAmount` | number | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetailInvoiceArrivalAccountCoded` | boolean | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetailInvoiceArrivalAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetailInvoiceArrivalDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetailInvoiceArrivalTime` | date | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetailInvoiceAsset` | boolean | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetailInvoiceAuthorizationRole` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetailInvoiceAuthorizationUser` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetailInvoiceBaseAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetailInvoiceBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetailInvoiceBaseNetAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetailInvoiceBaseVatAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetailInvoiceBlocked` | boolean | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetailInvoiceBuyingRate` | number | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetailInvoiceChTime` | date | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetailInvoiceChUser` | string | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetailInvoiceClassified` | boolean | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetailInvoiceCompany` | string | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetailInvoiceCompanyDTO` | object | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetailInvoiceCompanyDTOHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetailInvoiceCompanyDTOForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetailInvoiceCompanyDTOLocked` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetailInvoiceCompanyDTOLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetailInvoiceCompanyDTOLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetailInvoiceCompanyDTOLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetailInvoiceCompanyDTORowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetailInvoiceCompanyDTOSelected` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetailInvoiceCompanyDTOKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetailInvoiceCompanyDTOCompany` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetailInvoiceCompanyDTOName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetailInvoiceCompanyDTOType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetailInvoiceCompanyDTOValidTo` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetailInvoiceCompanyDTOInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetailInvoiceCompanyDTOBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetailInvoiceCompanyDTOVatNo` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetailInvoiceCompanyDTOPostalAddressId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetailInvoiceCompanyDTOWww` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetailInvoiceCompanyDTOContact` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetailInvoiceCompanyDTOEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetailInvoiceCompanyDTOErrorHandlingRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetailInvoiceCompanyDTOCheckRange` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetailInvoiceCompanyDTOCheckCounter` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetailInvoiceCompanyDTOCheckRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationIsActive` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOArrivalType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCoding` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetailInvoiceCompanyDTOAccountCodingDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetailInvoiceCompanyDTOCalculateDueDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetailInvoiceCompanyDTOSetAccountCodedBy` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetailInvoiceCompanyDTOPaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetailInvoiceCompanyDTOClassifySupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetailInvoiceCompanyDTODebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOCostAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetailInvoiceCompanyDTOVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetailInvoiceCompanyDTOSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetailInvoiceCompanyDTOGetVatCodeFrom` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetailInvoiceCompanyDTOVatAccountCodingType` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetailInvoiceCompanyDTOFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOUseReference` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAutoDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOErp` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetailInvoiceCompanyDTOGroup1` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetailInvoiceCompanyDTOGroup2` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetailInvoiceCompanyDTOGroup3` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOChTime` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetailInvoiceCompanyDTOChUser` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetailInvoiceCompanyDTODirectRecording` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetailInvoiceCompanyDTOVatExempt` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetailInvoiceCompanyDTOIdentifyBitCode` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetailInvoiceCompanyDTOExpenseInstantReminder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetailInvoiceCompanyDTOExpenseSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetailInvoiceCompanyDTORequisitionNoApproval` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetailInvoiceCompanyDTOEan` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetailInvoiceCompanyDTOUseBuyersHelp` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetailInvoiceCompanyDTOObjectType1Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType2Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType3Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType4Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType5Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType6Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType7Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType8Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTODeliveryCode` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetailInvoiceCompanyDTOAllocationSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetailInvoiceCompanyDTOAiInvoice` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetailInvoiceCompanyDTOSupplierMatchPattern` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetailInvoiceCompanyDTOVarianceVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetailInvoiceCompanyDTOMaxVarianceAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetailInvoiceCompanyDTOAiNoPrediction` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetailInvoiceCompanyDTOVat1AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat2AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat3AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat4AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTOContractNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTORillionCaptureUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetailInvoiceCompanyDTORillionCapturelabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceLabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetailInvoiceCompanyDTOUseAmountInRounding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetailInvoiceCompanyDTORoundingAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetailInvoiceCompanyDTOCompanyAlias` | array | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetailInvoiceCompanyName` | string | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetailInvoiceContractMatch` | number | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetailInvoiceContractNo` | string | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetailInvoiceCrDate` | date | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetailInvoiceCredit` | boolean | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetailInvoiceCreditTime` | number | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetailInvoiceCurrency` | string | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetailInvoiceCurrentLevel` | number | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetailInvoiceCurrentRole` | string | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetailInvoiceDeptAccountId` | number | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetailInvoiceDiscountAmount` | number | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetailInvoiceDiscountDate` | date | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetailInvoiceDiscountGrossAmount` | boolean | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetailInvoiceDiscountPercentage` | number | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetailInvoiceDueDate` | date | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetailInvoiceEmailSignRole` | string | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetailInvoiceExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetailInvoiceSystemCurrencyExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetailInvoiceExpenseMatch` | number | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetailInvoiceExtraAmount` | number | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetailInvoiceExtraId` | string | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetailInvoiceFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetailInvoiceFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetailInvoiceFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetailInvoiceFileTypeId` | number | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetailInvoiceFlowAddition` | number | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetailInvoiceFlowProposal` | string | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetailInvoiceFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetailInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetailInvoiceForPartialPayment` | boolean | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetailInvoiceGroup1` | string | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetailInvoiceGroup2` | string | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetailInvoiceGroup3` | string | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetailInvoiceGroup4` | string | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetailInvoiceGroup5` | string | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetailInvoiceGroup6` | string | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetailInvoiceInvestigate` | boolean | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetailInvoiceInvoiceAccountCodingAmount` | number | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetailInvoiceInvoiceDate` | date | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetailInvoiceInvoiceFlowId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetailInvoiceInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetailInvoiceInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetailInvoiceInvoiceImageFileExtension` | string | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetailInvoiceInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetailInvoiceInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetailInvoiceInvoiceStatusMessage` | string | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetailInvoiceIsContractMatch` | number | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetailInvoiceIsPurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetailInvoiceLatestDiaryNote` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetailInvoiceLatestDiaryNoteUser` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetailInvoiceLatestDiaryNoteTime` | date | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetailInvoiceLinkedInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetailInvoiceLinkedInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetailInvoiceLinkedInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetailInvoiceMatchedContractId` | number | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetailInvoiceNetAmount` | number | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetailInvoiceNoOfRoles` | number | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetailInvoiceObject1` | string | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetailInvoiceObject1Id` | number | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetailInvoiceObject1Name` | string | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetailInvoiceObject2` | string | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetailInvoiceObject2Id` | number | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetailInvoiceObject2Name` | string | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetailInvoiceObject3` | string | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetailInvoiceObject3Id` | number | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetailInvoiceObject3Name` | string | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetailInvoiceObject4` | string | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetailInvoiceObject4Id` | number | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetailInvoiceObject4Name` | string | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetailInvoiceObject5` | string | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetailInvoiceObject5Id` | number | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetailInvoiceObject5Name` | string | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetailInvoiceObject6` | string | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetailInvoiceObject6Id` | number | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetailInvoiceObject6Name` | string | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetailInvoiceObject7` | string | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetailInvoiceObject7Id` | number | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetailInvoiceObject7Name` | string | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetailInvoiceObject8` | string | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetailInvoiceObject8Id` | number | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetailInvoiceObject8Name` | string | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetailInvoiceOldAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetailInvoiceOriginalSupplierId` | number | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetailInvoiceOriginalSupplierName` | string | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetailInvoiceOriginalVatType` | string | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetailInvoicePartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetailInvoicePartialPaymentAmountUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetailInvoicePaymentDate` | date | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetailInvoicePaymentMessage` | string | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetailInvoicePaymentTerm` | string | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetailInvoicePaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetailInvoicePaymentTime` | number | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetailInvoicePayReference` | string | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetailInvoicePeriodAmount` | number | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetailInvoicePostingsUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetailInvoiceProcessDays` | number | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetailInvoiceProcessTime` | number | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetailInvoicePurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetailInvoicePurchaseOrderNo` | string | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetailInvoiceReference1` | string | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetailInvoiceReference2` | string | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetailInvoiceRemainingPartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetailInvoiceReminderReason` | number | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetailInvoiceRole` | string | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetailInvoiceShowDate` | date | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetailInvoiceStatus` | number | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetailInvoiceSupplier` | string | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetailInvoiceSupplierActiveCreditCard` | boolean | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetailInvoiceSupplierAddress1` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetailInvoiceSupplierAddress2` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetailInvoiceSupplierAddress3` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetailInvoiceSupplierAddress4` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetailInvoiceSupplierAddress5` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetailInvoiceSupplierAddress6` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetailInvoiceSupplierBankAccount` | string | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetailInvoiceSupplierDeliveryNote` | string | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetailInvoiceSupplierId` | number | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetailInvoiceSupplierInvoiceNo` | string | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetailInvoiceSupplierName` | string | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetailInvoiceNoOfImages` | number | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetailInvoiceTimestamp` | number | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetailInvoiceType` | number | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetailInvoiceUpdateSupplierOrAmount` | boolean | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetailInvoiceUseDiscount` | boolean | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetailInvoiceVatAmount` | number | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetailInvoiceVat1Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetailInvoiceVat2Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetailInvoiceVat3Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetailInvoiceVat4Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetailInvoiceVatCalculation` | boolean | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetailInvoiceVatCode` | string | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetailInvoiceVatCodeID` | number | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetailInvoiceVatType` | string | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetailInvoiceVatTypeId` | number | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetailInvoiceVoucherNo` | number | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetailInvoiceVoucherSeries` | string | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetailInvoiceExternalId` | string | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetailInvoiceExternalSource` | string | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetailInvoiceIsDynamicFlow` | boolean | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetailInvoiceAuthorizationAmountData` | object | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts` | array | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetailInvoiceAccountCodings` | array | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetailInvoiceFlows` | array | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetailInvoiceDiaries` | array | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetailObjectTypes` | array | yes | Request body value for InvoiceDetail ObjectTypes. |
| `invoiceDetail` | object | yes | Request body value for InvoiceDetail. |
| `invoiceDetailHeadersOnly` | number | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetailForProcessing` | boolean | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetailLocked` | boolean | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetailLockedRowId` | number | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetailLockedRowLoginName` | string | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetailLockedRowRole` | string | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetailRowState` | number | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetailSelected` | boolean | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetailKeyValuesRowState` | number | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetailInvoice` | object | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetailInvoiceHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetailInvoiceForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetailInvoiceLocked` | boolean | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetailInvoiceLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetailInvoiceLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetailInvoiceLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetailInvoiceRowState` | number | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetailInvoiceSelected` | boolean | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetailInvoiceKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetailInvoiceAccount` | string | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetailInvoiceAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetailInvoiceAccountCodingProposal` | string | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetailInvoiceAccountCodingProposalID` | number | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetailInvoiceAccountId` | number | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetailInvoiceAccountName` | string | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetailInvoiceAlternativeId` | string | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetailInvoiceAmount` | number | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetailInvoiceArrivalAccountCoded` | boolean | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetailInvoiceArrivalAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetailInvoiceArrivalDate` | date | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetailInvoiceArrivalTime` | date | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetailInvoiceAsset` | boolean | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetailInvoiceAuthorizationRole` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetailInvoiceAuthorizationUser` | string | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetailInvoiceBaseAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetailInvoiceBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetailInvoiceBaseNetAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetailInvoiceBaseVatAmount` | number | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetailInvoiceBlocked` | boolean | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetailInvoiceBuyingRate` | number | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetailInvoiceChTime` | date | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetailInvoiceChUser` | string | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetailInvoiceClassified` | boolean | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetailInvoiceCompany` | string | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetailInvoiceCompanyDTO` | object | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetailInvoiceCompanyDTOHeadersOnly` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetailInvoiceCompanyDTOForProcessing` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetailInvoiceCompanyDTOLocked` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetailInvoiceCompanyDTOLockedRowId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetailInvoiceCompanyDTOLockedRowLoginName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetailInvoiceCompanyDTOLockedRowRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetailInvoiceCompanyDTORowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetailInvoiceCompanyDTOSelected` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetailInvoiceCompanyDTOKeyValuesRowState` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetailInvoiceCompanyDTOCompany` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetailInvoiceCompanyDTOName` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetailInvoiceCompanyDTOType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetailInvoiceCompanyDTOValidTo` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetailInvoiceCompanyDTOInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetailInvoiceCompanyDTOBaseCurrency` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetailInvoiceCompanyDTOVatNo` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetailInvoiceCompanyDTOPostalAddressId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetailInvoiceCompanyDTOWww` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetailInvoiceCompanyDTOContact` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetailInvoiceCompanyDTOEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetailInvoiceCompanyDTOErrorHandlingRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetailInvoiceCompanyDTOCheckRange` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetailInvoiceCompanyDTOCheckCounter` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetailInvoiceCompanyDTOCheckRole` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationIsActive` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetailInvoiceCompanyDTOCodeRelationCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetailInvoiceCompanyDTOInvoicePermissionGroupCheck` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOBuyerPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOContractPermissionGroupCheck` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetailInvoiceCompanyDTOArrivalType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCoding` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetailInvoiceCompanyDTOAccountCodingDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetailInvoiceCompanyDTOCalculateDueDate` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetailInvoiceCompanyDTOSetAccountCodedBy` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetailInvoiceCompanyDTOPaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetailInvoiceCompanyDTOClassifySupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetailInvoiceCompanyDTODebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOCostAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetailInvoiceCompanyDTOVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetailInvoiceCompanyDTOUseAmountExcludingVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetailInvoiceCompanyDTOAuthorizationAmountTwoRoles` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetailInvoiceCompanyDTOSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetailInvoiceCompanyDTOCheckAuthorizationAmountConsiderSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetailInvoiceCompanyDTOSortAuthorizationAmountDescending` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetailInvoiceCompanyDTOAllocationsAmountLimit` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetailInvoiceCompanyDTOGetVatCodeFrom` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetailInvoiceCompanyDTOVatAccountCodingType` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetailInvoiceCompanyDTOFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOContractFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOUseReference` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowPercentExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationRowTotalAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOMatchDeviationVatAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAutoDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTORoleMatchedPurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowDeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIddeliveryPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPricePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpricePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowPurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdpurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchDeliveryEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceNoOfDays` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetailInvoiceCompanyDTOReMatchPriceEmail` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountExceed` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingAmountBelow` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetailInvoiceCompanyDTOAccountIdoutstandingVatAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOAccountIdfeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetailInvoiceCompanyDTOMaxFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetailInvoiceCompanyDTOErp` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetailInvoiceCompanyDTOGroup1` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetailInvoiceCompanyDTOGroup2` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetailInvoiceCompanyDTOGroup3` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSign` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetailInvoiceCompanyDTOCheckInvoiceIsSignPurchaseOrder` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOChTime` | date | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetailInvoiceCompanyDTOChUser` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetailInvoiceCompanyDTODirectRecording` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetailInvoiceCompanyDTOVatExempt` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetailInvoiceCompanyDTOCheckSumAccountcoding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetailInvoiceCompanyDTOIdentifyBitCode` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderEqualSupplier` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetailInvoiceCompanyDTOFlowMatchedLowConfidencePurchaseOrder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTOFlowProposalIdmatchedLowConfidencePurchaseOrder` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetailInvoiceCompanyDTONumberOfMonthsBetweenDuplicates` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetailInvoiceCompanyDTOAcceptedCurrencyVariance` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetailInvoiceCompanyDTOExpenseRoleMissingPaymentReceiver` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetailInvoiceCompanyDTOExpenseInstantReminder` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetailInvoiceCompanyDTOExpenseDebtAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetailInvoiceCompanyDTOExpenseUnknownSupplierId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetailInvoiceCompanyDTOExpenseSigningRule` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetailInvoiceCompanyDTORequisitionNoApproval` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetailInvoiceCompanyDTOEan` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetailInvoiceCompanyDTOPurchaseRequisitionSetAccountOutstandingAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetailInvoiceCompanyDTOCalculationChangedMatchedAmount` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetailInvoiceCompanyDTOCheckSumOfInvoiceLines` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetailInvoiceCompanyDTOUseBuyersHelp` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetailInvoiceCompanyDTOExpensePrivateAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetailInvoiceCompanyDTOAllocateDeviationTotalAmount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetailInvoiceCompanyDTORequisitionTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOExpenseAdvanceAsCredit` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetailInvoiceCompanyDTOObjectType1Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType2Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType3Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType4Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType5Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType6Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType7Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetailInvoiceCompanyDTOObjectType8Name` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetailInvoiceCompanyDTOCheckAmountForCreditNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetailInvoiceCompanyDTOExpenseVatfromMatch` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderDeliverySetDeliveryNote` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetailInvoiceCompanyDTOCheckDuplicateExpenses` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowAtUnknown` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetailInvoiceCompanyDTOExpenditureFlowProposalIdatUnknown` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetailInvoiceCompanyDTOAcceptPartialDelivery` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetailInvoiceCompanyDTORequisitionSubjectRequired` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetailInvoiceCompanyDTOAlwaysCalculateVat` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceTwoRolesApproval` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTOAllowPostingToCostAccount` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetailInvoiceCompanyDTOExpenseInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountPostingTwoRolesApproval` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetailInvoiceCompanyDTODeliveryCode` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetailInvoiceCompanyDTOExpenseAlwaysCalculateVat` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingLineNoSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetailInvoiceCompanyDTOAllocationSetting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetailInvoiceCompanyDTOCalculateVatamountOnCostLine` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetailInvoiceCompanyDTOCompressPostingsDeliveredSeperately` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference1Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingReference2Setting` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetailInvoiceCompanyDTOInvoiceAccountCodingUseDefaultObjectSetting` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetailInvoiceCompanyDTOAiInvoice` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetailInvoiceCompanyDTOAiInvoiceConfidenceTransfer` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetailInvoiceCompanyDTOArrivalAccountCodingUpdate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetailInvoiceCompanyDTOSupplierMatchPattern` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetailInvoiceCompanyDTOVatObjectTypeNo2` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetailInvoiceCompanyDTOCreateDeliveryReturns` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetailInvoiceCompanyDTOFlowAdditionCheckType` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetailInvoiceCompanyDTOVarianceVatAccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetailInvoiceCompanyDTOMaxVarianceAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetailInvoiceCompanyDTOAiNoPrediction` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetailInvoiceCompanyDTOUseObjectRelationFilter` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetailInvoiceCompanyDTOVat1AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat2AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat3AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetailInvoiceCompanyDTOVat4AccountId` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetailInvoiceCompanyDTOOnlyApplyAlMatchingResult` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetailInvoiceCompanyDTOUseAutomaticPomatching` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetailInvoiceCompanyDTOPurchaseOrderNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTOContractNoregexValidation` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetailInvoiceCompanyDTORillionCaptureUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetailInvoiceCompanyDTORillionCapturelabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceUrl` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetailInvoiceCompanyDTOEInvoiceLabel` | string | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetailInvoiceCompanyDTOUseAmountInRounding` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetailInvoiceCompanyDTORoundingAmount` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetailInvoiceCompanyDTOUseInvoiceDateForExchangeRate` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetailInvoiceCompanyDTOInvoiceFlowDelaySetting` | number | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetailInvoiceCompanyDTOCheckAllocationStartDateClosedPeriod` | boolean | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetailInvoiceCompanyDTOCompanyAlias` | array | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetailInvoiceCompanyName` | string | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetailInvoiceContractMatch` | number | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetailInvoiceContractNo` | string | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetailInvoiceCrDate` | date | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetailInvoiceCredit` | boolean | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetailInvoiceCreditTime` | number | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetailInvoiceCurrency` | string | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetailInvoiceCurrentLevel` | number | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetailInvoiceCurrentRole` | string | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetailInvoiceDeptAccountId` | number | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetailInvoiceDiscountAmount` | number | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetailInvoiceDiscountDate` | date | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetailInvoiceDiscountGrossAmount` | boolean | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetailInvoiceDiscountPercentage` | number | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetailInvoiceDueDate` | date | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetailInvoiceEmailSignRole` | string | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetailInvoiceExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetailInvoiceSystemCurrencyExchangeRate` | number | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetailInvoiceExpenseMatch` | number | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetailInvoiceExtraAmount` | number | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetailInvoiceExtraId` | string | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetailInvoiceFeeAmount1` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetailInvoiceFeeAmount2` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetailInvoiceFeeAmount3` | number | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetailInvoiceFileTypeId` | number | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetailInvoiceFlowAddition` | number | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetailInvoiceFlowProposal` | string | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetailInvoiceFlowProposalId` | number | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetailInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetailInvoiceForPartialPayment` | boolean | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetailInvoiceGroup1` | string | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetailInvoiceGroup2` | string | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetailInvoiceGroup3` | string | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetailInvoiceGroup4` | string | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetailInvoiceGroup5` | string | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetailInvoiceGroup6` | string | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetailInvoiceInvestigate` | boolean | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetailInvoiceInvoiceAccountCodingAmount` | number | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetailInvoiceInvoiceDate` | date | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetailInvoiceInvoiceFlowId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetailInvoiceInvoiceFlowStatus` | number | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetailInvoiceInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetailInvoiceInvoiceImageFileExtension` | string | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetailInvoiceInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetailInvoiceInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetailInvoiceInvoiceStatusMessage` | string | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetailInvoiceIsContractMatch` | number | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetailInvoiceIsPurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetailInvoiceLatestDiaryNote` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetailInvoiceLatestDiaryNoteUser` | string | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetailInvoiceLatestDiaryNoteTime` | date | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetailInvoiceLinkedInvoiceId` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetailInvoiceLinkedInvoiceNo` | number | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetailInvoiceLinkedInvoiceSeries` | string | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetailInvoiceMatchedContractId` | number | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetailInvoiceNetAmount` | number | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetailInvoiceNoOfRoles` | number | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetailInvoiceObject1` | string | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetailInvoiceObject1Id` | number | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetailInvoiceObject1Name` | string | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetailInvoiceObject2` | string | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetailInvoiceObject2Id` | number | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetailInvoiceObject2Name` | string | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetailInvoiceObject3` | string | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetailInvoiceObject3Id` | number | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetailInvoiceObject3Name` | string | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetailInvoiceObject4` | string | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetailInvoiceObject4Id` | number | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetailInvoiceObject4Name` | string | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetailInvoiceObject5` | string | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetailInvoiceObject5Id` | number | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetailInvoiceObject5Name` | string | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetailInvoiceObject6` | string | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetailInvoiceObject6Id` | number | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetailInvoiceObject6Name` | string | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetailInvoiceObject7` | string | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetailInvoiceObject7Id` | number | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetailInvoiceObject7Name` | string | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetailInvoiceObject8` | string | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetailInvoiceObject8Id` | number | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetailInvoiceObject8Name` | string | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetailInvoiceOldAccountCodingDate` | date | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetailInvoiceOriginalSupplierId` | number | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetailInvoiceOriginalSupplierName` | string | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetailInvoiceOriginalVatType` | string | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetailInvoicePartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetailInvoicePartialPaymentAmountUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetailInvoicePaymentDate` | date | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetailInvoicePaymentMessage` | string | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetailInvoicePaymentTerm` | string | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetailInvoicePaymentTermId` | number | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetailInvoicePaymentTime` | number | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetailInvoicePayReference` | string | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetailInvoicePeriodAmount` | number | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetailInvoicePostingsUpdated` | boolean | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetailInvoiceProcessDays` | number | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetailInvoiceProcessTime` | number | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetailInvoicePurchaseOrderMatch` | number | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetailInvoicePurchaseOrderNo` | string | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetailInvoiceReference1` | string | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetailInvoiceReference2` | string | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetailInvoiceRemainingPartialPaymentAmount` | number | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetailInvoiceReminderReason` | number | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetailInvoiceRole` | string | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetailInvoiceShowDate` | date | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetailInvoiceStatus` | number | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetailInvoiceSupplier` | string | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetailInvoiceSupplierActiveCreditCard` | boolean | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetailInvoiceSupplierAddress1` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetailInvoiceSupplierAddress2` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetailInvoiceSupplierAddress3` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetailInvoiceSupplierAddress4` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetailInvoiceSupplierAddress5` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetailInvoiceSupplierAddress6` | string | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetailInvoiceSupplierBankAccount` | string | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetailInvoiceSupplierDeliveryNote` | string | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetailInvoiceSupplierId` | number | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetailInvoiceSupplierInvoiceNo` | string | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetailInvoiceSupplierName` | string | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetailInvoiceNoOfImages` | number | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetailInvoiceTimestamp` | number | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetailInvoiceType` | number | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetailInvoiceUpdateSupplierOrAmount` | boolean | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetailInvoiceUseDiscount` | boolean | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetailInvoiceVatAmount` | number | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetailInvoiceVat1Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetailInvoiceVat2Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetailInvoiceVat3Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetailInvoiceVat4Amount` | number | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetailInvoiceVatCalculation` | boolean | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetailInvoiceVatCode` | string | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetailInvoiceVatCodeID` | number | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetailInvoiceVatType` | string | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetailInvoiceVatTypeId` | number | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetailInvoiceVoucherNo` | number | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetailInvoiceVoucherSeries` | string | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetailInvoiceExternalId` | string | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetailInvoiceExternalSource` | string | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetailInvoiceIsDynamicFlow` | boolean | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetailInvoiceAuthorizationAmountRequiredForNewFlowRoles` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetailInvoiceAuthorizationAmountData` | object | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetailInvoiceAuthorizationAmountDataGeneralAuthorizationAmount` | number | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetailInvoiceAuthorizationAmountDataRoleAuthorizationAmounts` | array | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetailInvoiceAccountCodings` | array | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetailInvoiceFlows` | array | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetailInvoiceDiaries` | array | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetailObjectTypes` | array | yes | Request body value for InvoiceDetail ObjectTypes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/detail` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-details.md) for the provider-specific parameters and requirements.

