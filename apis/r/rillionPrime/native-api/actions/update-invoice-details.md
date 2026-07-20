# Update Invoice Details with Rillion Prime

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/detail`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Invoice Details](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | query | `string` | no | Optional query value for Role. |
| `invoiceDetail` | body | `object` | yes | Request body value for InvoiceDetail. |
| `invoiceDetail.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetail.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetail.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetail.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetail.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetail.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetail.rowState` | body | `number` | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetail.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetail.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetail.invoice` | body | `object` | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetail.invoice.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetail.invoice.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetail.invoice.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetail.invoice.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetail.invoice.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetail.invoice.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetail.invoice.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetail.invoice.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetail.invoice.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetail.invoice.account` | body | `string` | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetail.invoice.accountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetail.invoice.accountCodingProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetail.invoice.accountCodingProposalID` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetail.invoice.accountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetail.invoice.accountName` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetail.invoice.alternativeId` | body | `string` | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetail.invoice.amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetail.invoice.arrivalAccountCoded` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetail.invoice.arrivalAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetail.invoice.arrivalDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetail.invoice.arrivalTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetail.invoice.asset` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetail.invoice.authorizationRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetail.invoice.authorizationUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetail.invoice.baseAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetail.invoice.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetail.invoice.baseNetAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetail.invoice.baseVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetail.invoice.blocked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetail.invoice.buyingRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetail.invoice.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetail.invoice.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetail.invoice.classified` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetail.invoice.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetail.invoice.companyDTO` | body | `object` | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetail.invoice.companyDTO.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetail.invoice.companyDTO.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetail.invoice.companyDTO.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetail.invoice.companyDTO.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetail.invoice.companyDTO.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetail.invoice.companyDTO.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetail.invoice.companyDTO.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetail.invoice.companyDTO.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetail.invoice.companyDTO.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetail.invoice.companyDTO.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetail.invoice.companyDTO.name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetail.invoice.companyDTO.type` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetail.invoice.companyDTO.validTo` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetail.invoice.companyDTO.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetail.invoice.companyDTO.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetail.invoice.companyDTO.vatNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetail.invoice.companyDTO.postalAddressId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetail.invoice.companyDTO.www` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetail.invoice.companyDTO.contact` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetail.invoice.companyDTO.email` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetail.invoice.companyDTO.errorHandlingRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetail.invoice.companyDTO.checkRange` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetail.invoice.companyDTO.checkCounter` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetail.invoice.companyDTO.checkRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetail.invoice.companyDTO.codeRelationIsActive` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetail.invoice.companyDTO.codeRelationCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetail.invoice.companyDTO.invoicePermissionGroupCheck` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.buyerPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.contractPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.arrivalType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCoding` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetail.invoice.companyDTO.accountCodingDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetail.invoice.companyDTO.calculateDueDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetail.invoice.companyDTO.setAccountCodedBy` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetail.invoice.companyDTO.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetail.invoice.companyDTO.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetail.invoice.companyDTO.allocationsAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetail.invoice.companyDTO.classifySupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetail.invoice.companyDTO.debtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetail.invoice.companyDTO.costAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetail.invoice.companyDTO.vatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetail.invoice.companyDTO.useAmountExcludingVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetail.invoice.companyDTO.authorizationAmountTwoRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetail.invoice.companyDTO.signingRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetail.invoice.companyDTO.checkAuthorizationAmountConsiderSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetail.invoice.companyDTO.sortAuthorizationAmountDescending` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetail.invoice.companyDTO.allocationsAmountLimit` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetail.invoice.companyDTO.getVatCodeFrom` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetail.invoice.companyDTO.vatAccountCodingType` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetail.invoice.companyDTO.flowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.useReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetail.invoice.companyDTO.autoDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetail.invoice.companyDTO.flowMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.roleMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowDeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIddeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPricePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpricePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetail.invoice.companyDTO.erp` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetail.invoice.companyDTO.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetail.invoice.companyDTO.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetail.invoice.companyDTO.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSignPurchaseOrder` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetail.invoice.companyDTO.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetail.invoice.companyDTO.directRecording` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetail.invoice.companyDTO.vatExempt` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetail.invoice.companyDTO.checkSumAccountcoding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetail.invoice.companyDTO.identifyBitCode` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderEqualSupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetail.invoice.companyDTO.flowMatchedLowConfidencePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedLowConfidencePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.numberOfMonthsBetweenDuplicates` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetail.invoice.companyDTO.acceptedCurrencyVariance` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetail.invoice.companyDTO.expenseRoleMissingPaymentReceiver` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetail.invoice.companyDTO.expenseInstantReminder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetail.invoice.companyDTO.expenseDebtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetail.invoice.companyDTO.expenseUnknownSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetail.invoice.companyDTO.expenseSigningRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetail.invoice.companyDTO.requisitionNoApproval` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetail.invoice.companyDTO.ean` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionSetAccountOutstandingAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetail.invoice.companyDTO.calculationChangedMatchedAmount` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetail.invoice.companyDTO.checkSumOfInvoiceLines` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetail.invoice.companyDTO.useBuyersHelp` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetail.invoice.companyDTO.expensePrivateAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetail.invoice.companyDTO.allocateDeviationTotalAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetail.invoice.companyDTO.requisitionTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.expenseAdvanceAsCredit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetail.invoice.companyDTO.objectType1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetail.invoice.companyDTO.objectType2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetail.invoice.companyDTO.objectType3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetail.invoice.companyDTO.objectType4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetail.invoice.companyDTO.objectType5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetail.invoice.companyDTO.objectType6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetail.invoice.companyDTO.objectType7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetail.invoice.companyDTO.objectType8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetail.invoice.companyDTO.checkAmountForCreditNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetail.invoice.companyDTO.expenseVatfromMatch` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderDeliverySetDeliveryNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetail.invoice.companyDTO.checkDuplicateExpenses` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.acceptPartialDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetail.invoice.companyDTO.requisitionSubjectRequired` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetail.invoice.companyDTO.alwaysCalculateVat` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceTwoRolesApproval` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.allowPostingToCostAccount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetail.invoice.companyDTO.expenseInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountPostingTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.deliveryCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetail.invoice.companyDTO.expenseAlwaysCalculateVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingLineNoSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetail.invoice.companyDTO.allocationSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetail.invoice.companyDTO.calculateVatamountOnCostLine` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetail.invoice.companyDTO.compressPostingsDeliveredSeperately` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference1Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference2Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingUseDefaultObjectSetting` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetail.invoice.companyDTO.aiInvoice` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetail.invoice.companyDTO.aiInvoiceConfidenceTransfer` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCodingUpdate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetail.invoice.companyDTO.supplierMatchPattern` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetail.invoice.companyDTO.createDeliveryReturns` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetail.invoice.companyDTO.flowAdditionCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetail.invoice.companyDTO.varianceVatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetail.invoice.companyDTO.maxVarianceAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetail.invoice.companyDTO.aiNoPrediction` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetail.invoice.companyDTO.useObjectRelationFilter` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetail.invoice.companyDTO.vat1AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetail.invoice.companyDTO.vat2AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetail.invoice.companyDTO.vat3AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetail.invoice.companyDTO.vat4AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetail.invoice.companyDTO.onlyApplyAlMatchingResult` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetail.invoice.companyDTO.useAutomaticPomatching` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.contractNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.rillionCaptureUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetail.invoice.companyDTO.rillionCapturelabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetail.invoice.companyDTO.eInvoiceUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetail.invoice.companyDTO.eInvoiceLabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetail.invoice.companyDTO.useAmountInRounding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetail.invoice.companyDTO.roundingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetail.invoice.companyDTO.useInvoiceDateForExchangeRate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetail.invoice.companyDTO.invoiceFlowDelaySetting` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetail.invoice.companyDTO.checkAllocationStartDateClosedPeriod` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetail.invoice.companyDTO.companyAlias` | body | `array` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetail.invoice.companyName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetail.invoice.contractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetail.invoice.contractNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetail.invoice.crDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetail.invoice.credit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetail.invoice.creditTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetail.invoice.currency` | body | `string` | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetail.invoice.currentLevel` | body | `number` | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetail.invoice.currentRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetail.invoice.deptAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetail.invoice.discountAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetail.invoice.discountDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetail.invoice.discountGrossAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetail.invoice.discountPercentage` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetail.invoice.dueDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetail.invoice.emailSignRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetail.invoice.exchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetail.invoice.systemCurrencyExchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetail.invoice.expenseMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetail.invoice.extraAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetail.invoice.extraId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetail.invoice.feeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetail.invoice.feeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetail.invoice.feeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetail.invoice.fileTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetail.invoice.flowAddition` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetail.invoice.flowProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetail.invoice.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetail.invoice.flowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetail.invoice.forPartialPayment` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetail.invoice.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetail.invoice.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetail.invoice.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetail.invoice.group4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetail.invoice.group5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetail.invoice.group6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetail.invoice.investigate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetail.invoice.invoiceAccountCodingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetail.invoice.invoiceDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetail.invoice.invoiceFlowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetail.invoice.invoiceFlowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetail.invoice.invoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetail.invoice.invoiceImageFileExtension` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetail.invoice.invoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetail.invoice.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetail.invoice.invoiceStatusMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetail.invoice.isContractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetail.invoice.isPurchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetail.invoice.latestDiaryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetail.invoice.latestDiaryNoteUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetail.invoice.latestDiaryNoteTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetail.invoice.linkedInvoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetail.invoice.linkedInvoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetail.invoice.linkedInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetail.invoice.matchedContractId` | body | `number` | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetail.invoice.netAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetail.invoice.noOfRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetail.invoice.object1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetail.invoice.object1Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetail.invoice.object1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetail.invoice.object2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetail.invoice.object2Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetail.invoice.object2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetail.invoice.object3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetail.invoice.object3Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetail.invoice.object3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetail.invoice.object4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetail.invoice.object4Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetail.invoice.object4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetail.invoice.object5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetail.invoice.object5Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetail.invoice.object5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetail.invoice.object6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetail.invoice.object6Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetail.invoice.object6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetail.invoice.object7` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetail.invoice.object7Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetail.invoice.object7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetail.invoice.object8` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetail.invoice.object8Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetail.invoice.object8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetail.invoice.oldAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetail.invoice.originalSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetail.invoice.originalSupplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetail.invoice.originalVatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetail.invoice.partialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetail.invoice.partialPaymentAmountUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetail.invoice.paymentDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetail.invoice.paymentMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetail.invoice.paymentTerm` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetail.invoice.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetail.invoice.paymentTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetail.invoice.payReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetail.invoice.periodAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetail.invoice.postingsUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetail.invoice.processDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetail.invoice.processTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetail.invoice.purchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetail.invoice.purchaseOrderNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetail.invoice.reference1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetail.invoice.reference2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetail.invoice.remainingPartialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetail.invoice.reminderReason` | body | `number` | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetail.invoice.role` | body | `string` | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetail.invoice.showDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetail.invoice.status` | body | `number` | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetail.invoice.supplier` | body | `string` | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetail.invoice.supplierActiveCreditCard` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetail.invoice.supplierAddress1` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetail.invoice.supplierAddress2` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetail.invoice.supplierAddress3` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetail.invoice.supplierAddress4` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetail.invoice.supplierAddress5` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetail.invoice.supplierAddress6` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetail.invoice.supplierBankAccount` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetail.invoice.supplierDeliveryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetail.invoice.supplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetail.invoice.supplierInvoiceNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetail.invoice.supplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetail.invoice.noOfImages` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetail.invoice.timestamp` | body | `number` | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetail.invoice.type` | body | `number` | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetail.invoice.updateSupplierOrAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetail.invoice.useDiscount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetail.invoice.vatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetail.invoice.vat1Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetail.invoice.vat2Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetail.invoice.vat3Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetail.invoice.vat4Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetail.invoice.vatCalculation` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetail.invoice.vatCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetail.invoice.vatCodeID` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetail.invoice.vatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetail.invoice.vatTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetail.invoice.voucherNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetail.invoice.voucherSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetail.invoice.externalId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetail.invoice.externalSource` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetail.invoice.isDynamicFlow` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetail.invoice.authorizationAmountRequiredForNewFlowRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetail.invoice.authorizationAmountData` | body | `object` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetail.invoice.authorizationAmountData.generalAuthorizationAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetail.invoice.authorizationAmountData.roleAuthorizationAmounts` | body | `array` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetail.invoiceAccountCodings` | body | `array` | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetail.invoiceFlows` | body | `array` | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetail.invoiceDiaries` | body | `array` | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetail.objectTypes` | body | `array` | yes | Request body value for InvoiceDetail ObjectTypes. |
| `invoiceDetail` | body | `object` | yes | Request body value for InvoiceDetail. |
| `invoiceDetail.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetail.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetail.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetail.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetail.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetail.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetail.rowState` | body | `number` | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetail.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetail.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetail.invoice` | body | `object` | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetail.invoice.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetail.invoice.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetail.invoice.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetail.invoice.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetail.invoice.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetail.invoice.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetail.invoice.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetail.invoice.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetail.invoice.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetail.invoice.account` | body | `string` | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetail.invoice.accountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetail.invoice.accountCodingProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetail.invoice.accountCodingProposalID` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetail.invoice.accountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetail.invoice.accountName` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetail.invoice.alternativeId` | body | `string` | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetail.invoice.amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetail.invoice.arrivalAccountCoded` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetail.invoice.arrivalAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetail.invoice.arrivalDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetail.invoice.arrivalTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetail.invoice.asset` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetail.invoice.authorizationRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetail.invoice.authorizationUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetail.invoice.baseAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetail.invoice.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetail.invoice.baseNetAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetail.invoice.baseVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetail.invoice.blocked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetail.invoice.buyingRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetail.invoice.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetail.invoice.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetail.invoice.classified` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetail.invoice.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetail.invoice.companyDTO` | body | `object` | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetail.invoice.companyDTO.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetail.invoice.companyDTO.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetail.invoice.companyDTO.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetail.invoice.companyDTO.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetail.invoice.companyDTO.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetail.invoice.companyDTO.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetail.invoice.companyDTO.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetail.invoice.companyDTO.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetail.invoice.companyDTO.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetail.invoice.companyDTO.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetail.invoice.companyDTO.name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetail.invoice.companyDTO.type` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetail.invoice.companyDTO.validTo` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetail.invoice.companyDTO.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetail.invoice.companyDTO.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetail.invoice.companyDTO.vatNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetail.invoice.companyDTO.postalAddressId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetail.invoice.companyDTO.www` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetail.invoice.companyDTO.contact` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetail.invoice.companyDTO.email` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetail.invoice.companyDTO.errorHandlingRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetail.invoice.companyDTO.checkRange` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetail.invoice.companyDTO.checkCounter` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetail.invoice.companyDTO.checkRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetail.invoice.companyDTO.codeRelationIsActive` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetail.invoice.companyDTO.codeRelationCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetail.invoice.companyDTO.invoicePermissionGroupCheck` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.buyerPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.contractPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.arrivalType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCoding` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetail.invoice.companyDTO.accountCodingDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetail.invoice.companyDTO.calculateDueDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetail.invoice.companyDTO.setAccountCodedBy` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetail.invoice.companyDTO.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetail.invoice.companyDTO.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetail.invoice.companyDTO.allocationsAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetail.invoice.companyDTO.classifySupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetail.invoice.companyDTO.debtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetail.invoice.companyDTO.costAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetail.invoice.companyDTO.vatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetail.invoice.companyDTO.useAmountExcludingVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetail.invoice.companyDTO.authorizationAmountTwoRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetail.invoice.companyDTO.signingRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetail.invoice.companyDTO.checkAuthorizationAmountConsiderSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetail.invoice.companyDTO.sortAuthorizationAmountDescending` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetail.invoice.companyDTO.allocationsAmountLimit` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetail.invoice.companyDTO.getVatCodeFrom` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetail.invoice.companyDTO.vatAccountCodingType` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetail.invoice.companyDTO.flowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.useReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetail.invoice.companyDTO.autoDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetail.invoice.companyDTO.flowMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.roleMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowDeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIddeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPricePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpricePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetail.invoice.companyDTO.erp` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetail.invoice.companyDTO.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetail.invoice.companyDTO.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetail.invoice.companyDTO.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSignPurchaseOrder` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetail.invoice.companyDTO.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetail.invoice.companyDTO.directRecording` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetail.invoice.companyDTO.vatExempt` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetail.invoice.companyDTO.checkSumAccountcoding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetail.invoice.companyDTO.identifyBitCode` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderEqualSupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetail.invoice.companyDTO.flowMatchedLowConfidencePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedLowConfidencePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.numberOfMonthsBetweenDuplicates` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetail.invoice.companyDTO.acceptedCurrencyVariance` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetail.invoice.companyDTO.expenseRoleMissingPaymentReceiver` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetail.invoice.companyDTO.expenseInstantReminder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetail.invoice.companyDTO.expenseDebtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetail.invoice.companyDTO.expenseUnknownSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetail.invoice.companyDTO.expenseSigningRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetail.invoice.companyDTO.requisitionNoApproval` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetail.invoice.companyDTO.ean` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionSetAccountOutstandingAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetail.invoice.companyDTO.calculationChangedMatchedAmount` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetail.invoice.companyDTO.checkSumOfInvoiceLines` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetail.invoice.companyDTO.useBuyersHelp` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetail.invoice.companyDTO.expensePrivateAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetail.invoice.companyDTO.allocateDeviationTotalAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetail.invoice.companyDTO.requisitionTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.expenseAdvanceAsCredit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetail.invoice.companyDTO.objectType1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetail.invoice.companyDTO.objectType2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetail.invoice.companyDTO.objectType3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetail.invoice.companyDTO.objectType4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetail.invoice.companyDTO.objectType5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetail.invoice.companyDTO.objectType6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetail.invoice.companyDTO.objectType7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetail.invoice.companyDTO.objectType8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetail.invoice.companyDTO.checkAmountForCreditNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetail.invoice.companyDTO.expenseVatfromMatch` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderDeliverySetDeliveryNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetail.invoice.companyDTO.checkDuplicateExpenses` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.acceptPartialDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetail.invoice.companyDTO.requisitionSubjectRequired` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetail.invoice.companyDTO.alwaysCalculateVat` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceTwoRolesApproval` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.allowPostingToCostAccount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetail.invoice.companyDTO.expenseInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountPostingTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.deliveryCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetail.invoice.companyDTO.expenseAlwaysCalculateVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingLineNoSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetail.invoice.companyDTO.allocationSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetail.invoice.companyDTO.calculateVatamountOnCostLine` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetail.invoice.companyDTO.compressPostingsDeliveredSeperately` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference1Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference2Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingUseDefaultObjectSetting` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetail.invoice.companyDTO.aiInvoice` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetail.invoice.companyDTO.aiInvoiceConfidenceTransfer` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCodingUpdate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetail.invoice.companyDTO.supplierMatchPattern` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetail.invoice.companyDTO.createDeliveryReturns` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetail.invoice.companyDTO.flowAdditionCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetail.invoice.companyDTO.varianceVatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetail.invoice.companyDTO.maxVarianceAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetail.invoice.companyDTO.aiNoPrediction` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetail.invoice.companyDTO.useObjectRelationFilter` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetail.invoice.companyDTO.vat1AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetail.invoice.companyDTO.vat2AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetail.invoice.companyDTO.vat3AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetail.invoice.companyDTO.vat4AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetail.invoice.companyDTO.onlyApplyAlMatchingResult` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetail.invoice.companyDTO.useAutomaticPomatching` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.contractNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.rillionCaptureUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetail.invoice.companyDTO.rillionCapturelabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetail.invoice.companyDTO.eInvoiceUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetail.invoice.companyDTO.eInvoiceLabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetail.invoice.companyDTO.useAmountInRounding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetail.invoice.companyDTO.roundingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetail.invoice.companyDTO.useInvoiceDateForExchangeRate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetail.invoice.companyDTO.invoiceFlowDelaySetting` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetail.invoice.companyDTO.checkAllocationStartDateClosedPeriod` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetail.invoice.companyDTO.companyAlias` | body | `array` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetail.invoice.companyName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetail.invoice.contractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetail.invoice.contractNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetail.invoice.crDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetail.invoice.credit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetail.invoice.creditTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetail.invoice.currency` | body | `string` | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetail.invoice.currentLevel` | body | `number` | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetail.invoice.currentRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetail.invoice.deptAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetail.invoice.discountAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetail.invoice.discountDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetail.invoice.discountGrossAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetail.invoice.discountPercentage` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetail.invoice.dueDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetail.invoice.emailSignRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetail.invoice.exchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetail.invoice.systemCurrencyExchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetail.invoice.expenseMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetail.invoice.extraAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetail.invoice.extraId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetail.invoice.feeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetail.invoice.feeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetail.invoice.feeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetail.invoice.fileTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetail.invoice.flowAddition` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetail.invoice.flowProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetail.invoice.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetail.invoice.flowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetail.invoice.forPartialPayment` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetail.invoice.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetail.invoice.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetail.invoice.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetail.invoice.group4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetail.invoice.group5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetail.invoice.group6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetail.invoice.investigate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetail.invoice.invoiceAccountCodingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetail.invoice.invoiceDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetail.invoice.invoiceFlowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetail.invoice.invoiceFlowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetail.invoice.invoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetail.invoice.invoiceImageFileExtension` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetail.invoice.invoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetail.invoice.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetail.invoice.invoiceStatusMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetail.invoice.isContractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetail.invoice.isPurchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetail.invoice.latestDiaryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetail.invoice.latestDiaryNoteUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetail.invoice.latestDiaryNoteTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetail.invoice.linkedInvoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetail.invoice.linkedInvoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetail.invoice.linkedInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetail.invoice.matchedContractId` | body | `number` | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetail.invoice.netAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetail.invoice.noOfRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetail.invoice.object1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetail.invoice.object1Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetail.invoice.object1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetail.invoice.object2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetail.invoice.object2Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetail.invoice.object2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetail.invoice.object3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetail.invoice.object3Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetail.invoice.object3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetail.invoice.object4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetail.invoice.object4Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetail.invoice.object4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetail.invoice.object5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetail.invoice.object5Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetail.invoice.object5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetail.invoice.object6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetail.invoice.object6Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetail.invoice.object6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetail.invoice.object7` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetail.invoice.object7Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetail.invoice.object7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetail.invoice.object8` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetail.invoice.object8Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetail.invoice.object8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetail.invoice.oldAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetail.invoice.originalSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetail.invoice.originalSupplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetail.invoice.originalVatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetail.invoice.partialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetail.invoice.partialPaymentAmountUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetail.invoice.paymentDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetail.invoice.paymentMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetail.invoice.paymentTerm` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetail.invoice.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetail.invoice.paymentTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetail.invoice.payReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetail.invoice.periodAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetail.invoice.postingsUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetail.invoice.processDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetail.invoice.processTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetail.invoice.purchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetail.invoice.purchaseOrderNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetail.invoice.reference1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetail.invoice.reference2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetail.invoice.remainingPartialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetail.invoice.reminderReason` | body | `number` | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetail.invoice.role` | body | `string` | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetail.invoice.showDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetail.invoice.status` | body | `number` | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetail.invoice.supplier` | body | `string` | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetail.invoice.supplierActiveCreditCard` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetail.invoice.supplierAddress1` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetail.invoice.supplierAddress2` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetail.invoice.supplierAddress3` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetail.invoice.supplierAddress4` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetail.invoice.supplierAddress5` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetail.invoice.supplierAddress6` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetail.invoice.supplierBankAccount` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetail.invoice.supplierDeliveryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetail.invoice.supplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetail.invoice.supplierInvoiceNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetail.invoice.supplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetail.invoice.noOfImages` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetail.invoice.timestamp` | body | `number` | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetail.invoice.type` | body | `number` | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetail.invoice.updateSupplierOrAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetail.invoice.useDiscount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetail.invoice.vatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetail.invoice.vat1Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetail.invoice.vat2Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetail.invoice.vat3Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetail.invoice.vat4Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetail.invoice.vatCalculation` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetail.invoice.vatCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetail.invoice.vatCodeID` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetail.invoice.vatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetail.invoice.vatTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetail.invoice.voucherNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetail.invoice.voucherSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetail.invoice.externalId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetail.invoice.externalSource` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetail.invoice.isDynamicFlow` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetail.invoice.authorizationAmountRequiredForNewFlowRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetail.invoice.authorizationAmountData` | body | `object` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetail.invoice.authorizationAmountData.generalAuthorizationAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetail.invoice.authorizationAmountData.roleAuthorizationAmounts` | body | `array` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetail.invoiceAccountCodings` | body | `array` | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetail.invoiceFlows` | body | `array` | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetail.invoiceDiaries` | body | `array` | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetail.objectTypes` | body | `array` | yes | Request body value for InvoiceDetail ObjectTypes. |
| `invoiceDetail` | body | `object` | yes | Request body value for InvoiceDetail. |
| `invoiceDetail.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail HeadersOnly. |
| `invoiceDetail.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail ForProcessing. |
| `invoiceDetail.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Locked. |
| `invoiceDetail.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail LockedRowId. |
| `invoiceDetail.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail LockedRowLoginName. |
| `invoiceDetail.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail LockedRowRole. |
| `invoiceDetail.rowState` | body | `number` | yes | Request body value for InvoiceDetail RowState. |
| `invoiceDetail.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Selected. |
| `invoiceDetail.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail KeyValuesRowState. |
| `invoiceDetail.invoice` | body | `object` | yes | Request body value for InvoiceDetail Invoice. |
| `invoiceDetail.invoice.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice HeadersOnly. |
| `invoiceDetail.invoice.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForProcessing. |
| `invoiceDetail.invoice.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Locked. |
| `invoiceDetail.invoice.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LockedRowId. |
| `invoiceDetail.invoice.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowLoginName. |
| `invoiceDetail.invoice.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice LockedRowRole. |
| `invoiceDetail.invoice.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice RowState. |
| `invoiceDetail.invoice.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Selected. |
| `invoiceDetail.invoice.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice KeyValuesRowState. |
| `invoiceDetail.invoice.account` | body | `string` | yes | Request body value for InvoiceDetail Invoice Account. |
| `invoiceDetail.invoice.accountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice AccountCodingDate. |
| `invoiceDetail.invoice.accountCodingProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposal. |
| `invoiceDetail.invoice.accountCodingProposalID` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountCodingProposalID. |
| `invoiceDetail.invoice.accountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice AccountId. |
| `invoiceDetail.invoice.accountName` | body | `string` | yes | Request body value for InvoiceDetail Invoice AccountName. |
| `invoiceDetail.invoice.alternativeId` | body | `string` | yes | Request body value for InvoiceDetail Invoice AlternativeId. |
| `invoiceDetail.invoice.amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Amount. |
| `invoiceDetail.invoice.arrivalAccountCoded` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCoded. |
| `invoiceDetail.invoice.arrivalAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalAccountCodingDate. |
| `invoiceDetail.invoice.arrivalDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalDate. |
| `invoiceDetail.invoice.arrivalTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ArrivalTime. |
| `invoiceDetail.invoice.asset` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Asset. |
| `invoiceDetail.invoice.authorizationRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationRole. |
| `invoiceDetail.invoice.authorizationUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice AuthorizationUser. |
| `invoiceDetail.invoice.baseAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseAmount. |
| `invoiceDetail.invoice.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice BaseCurrency. |
| `invoiceDetail.invoice.baseNetAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseNetAmount. |
| `invoiceDetail.invoice.baseVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice BaseVatAmount. |
| `invoiceDetail.invoice.blocked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Blocked. |
| `invoiceDetail.invoice.buyingRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice BuyingRate. |
| `invoiceDetail.invoice.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice ChTime. |
| `invoiceDetail.invoice.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice ChUser. |
| `invoiceDetail.invoice.classified` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Classified. |
| `invoiceDetail.invoice.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice Company. |
| `invoiceDetail.invoice.companyDTO` | body | `object` | yes | Request body value for InvoiceDetail Invoice CompanyDTO. |
| `invoiceDetail.invoice.companyDTO.headersOnly` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO HeadersOnly. |
| `invoiceDetail.invoice.companyDTO.forProcessing` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ForProcessing. |
| `invoiceDetail.invoice.companyDTO.locked` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Locked. |
| `invoiceDetail.invoice.companyDTO.lockedRowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowId. |
| `invoiceDetail.invoice.companyDTO.lockedRowLoginName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowLoginName. |
| `invoiceDetail.invoice.companyDTO.lockedRowRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO LockedRowRole. |
| `invoiceDetail.invoice.companyDTO.rowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RowState. |
| `invoiceDetail.invoice.companyDTO.selected` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Selected. |
| `invoiceDetail.invoice.companyDTO.keyValuesRowState` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO KeyValuesRowState. |
| `invoiceDetail.invoice.companyDTO.company` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Company. |
| `invoiceDetail.invoice.companyDTO.name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Name. |
| `invoiceDetail.invoice.companyDTO.type` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Type. |
| `invoiceDetail.invoice.companyDTO.validTo` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ValidTo. |
| `invoiceDetail.invoice.companyDTO.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderSeries. |
| `invoiceDetail.invoice.companyDTO.baseCurrency` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BaseCurrency. |
| `invoiceDetail.invoice.companyDTO.vatNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatNo. |
| `invoiceDetail.invoice.companyDTO.postalAddressId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PostalAddressId. |
| `invoiceDetail.invoice.companyDTO.www` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Www. |
| `invoiceDetail.invoice.companyDTO.contact` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Contact. |
| `invoiceDetail.invoice.companyDTO.email` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Email. |
| `invoiceDetail.invoice.companyDTO.errorHandlingRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ErrorHandlingRole. |
| `invoiceDetail.invoice.companyDTO.checkRange` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRange. |
| `invoiceDetail.invoice.companyDTO.checkCounter` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckCounter. |
| `invoiceDetail.invoice.companyDTO.checkRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckRole. |
| `invoiceDetail.invoice.companyDTO.codeRelationIsActive` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationIsActive. |
| `invoiceDetail.invoice.companyDTO.codeRelationCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CodeRelationCheckType. |
| `invoiceDetail.invoice.companyDTO.invoicePermissionGroupCheck` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoicePermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.buyerPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO BuyerPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.contractPermissionGroupCheck` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractPermissionGroupCheck. |
| `invoiceDetail.invoice.companyDTO.arrivalType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalType. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCoding` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCoding. |
| `invoiceDetail.invoice.companyDTO.accountCodingDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountCodingDate. |
| `invoiceDetail.invoice.companyDTO.calculateDueDate` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateDueDate. |
| `invoiceDetail.invoice.companyDTO.setAccountCodedBy` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SetAccountCodedBy. |
| `invoiceDetail.invoice.companyDTO.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalId. |
| `invoiceDetail.invoice.companyDTO.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PaymentTermId. |
| `invoiceDetail.invoice.companyDTO.allocationsAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAccountId. |
| `invoiceDetail.invoice.companyDTO.classifySupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ClassifySupplier. |
| `invoiceDetail.invoice.companyDTO.debtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DebtAccountId. |
| `invoiceDetail.invoice.companyDTO.costAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CostAccountId. |
| `invoiceDetail.invoice.companyDTO.vatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountId. |
| `invoiceDetail.invoice.companyDTO.useAmountExcludingVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountExcludingVat. |
| `invoiceDetail.invoice.companyDTO.authorizationAmountTwoRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AuthorizationAmountTwoRoles. |
| `invoiceDetail.invoice.companyDTO.signingRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SigningRule. |
| `invoiceDetail.invoice.companyDTO.checkAuthorizationAmountConsiderSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAuthorizationAmountConsiderSign. |
| `invoiceDetail.invoice.companyDTO.sortAuthorizationAmountDescending` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SortAuthorizationAmountDescending. |
| `invoiceDetail.invoice.companyDTO.allocationsAmountLimit` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationsAmountLimit. |
| `invoiceDetail.invoice.companyDTO.getVatCodeFrom` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO GetVatCodeFrom. |
| `invoiceDetail.invoice.companyDTO.vatAccountCodingType` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatAccountCodingType. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo. |
| `invoiceDetail.invoice.companyDTO.flowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.contractFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.useReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseReference. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowPercentExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowPercentExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationRowTotalAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationRowTotalAmountExceed. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountBelow. |
| `invoiceDetail.invoice.companyDTO.matchDeviationVatAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MatchDeviationVatAmountExceed. |
| `invoiceDetail.invoice.companyDTO.autoDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AutoDelivery. |
| `invoiceDetail.invoice.companyDTO.flowMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.roleMatchedPurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoleMatchedPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowDeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowDeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIddeliveryPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIddeliveryPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPricePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpricePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpricePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowPurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdpurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdpurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchDeliveryEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchDeliveryEmail. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceNoOfDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceNoOfDays. |
| `invoiceDetail.invoice.companyDTO.reMatchPriceEmail` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ReMatchPriceEmail. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountExceed` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountExceed. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingAmountBelow` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingAmountBelow. |
| `invoiceDetail.invoice.companyDTO.accountIdoutstandingVatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdoutstandingVatAmount. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount1. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount2. |
| `invoiceDetail.invoice.companyDTO.accountIdfeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AccountIdfeeAmount3. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount1. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount2. |
| `invoiceDetail.invoice.companyDTO.maxFeeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxFeeAmount3. |
| `invoiceDetail.invoice.companyDTO.erp` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Erp. |
| `invoiceDetail.invoice.companyDTO.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group1. |
| `invoiceDetail.invoice.companyDTO.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group2. |
| `invoiceDetail.invoice.companyDTO.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Group3. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSign` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSign. |
| `invoiceDetail.invoice.companyDTO.checkInvoiceIsSignPurchaseOrder` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckInvoiceIsSignPurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.chTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChTime. |
| `invoiceDetail.invoice.companyDTO.chUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ChUser. |
| `invoiceDetail.invoice.companyDTO.directRecording` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DirectRecording. |
| `invoiceDetail.invoice.companyDTO.vatExempt` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatExempt. |
| `invoiceDetail.invoice.companyDTO.checkSumAccountcoding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumAccountcoding. |
| `invoiceDetail.invoice.companyDTO.identifyBitCode` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO IdentifyBitCode. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderEqualSupplier` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderEqualSupplier. |
| `invoiceDetail.invoice.companyDTO.flowMatchedLowConfidencePurchaseOrder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowMatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.flowProposalIdmatchedLowConfidencePurchaseOrder` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowProposalIdmatchedLowConfidencePurchaseOrder. |
| `invoiceDetail.invoice.companyDTO.numberOfMonthsBetweenDuplicates` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO NumberOfMonthsBetweenDuplicates. |
| `invoiceDetail.invoice.companyDTO.acceptedCurrencyVariance` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptedCurrencyVariance. |
| `invoiceDetail.invoice.companyDTO.expenseRoleMissingPaymentReceiver` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseRoleMissingPaymentReceiver. |
| `invoiceDetail.invoice.companyDTO.expenseInstantReminder` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInstantReminder. |
| `invoiceDetail.invoice.companyDTO.expenseDebtAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseDebtAccountId. |
| `invoiceDetail.invoice.companyDTO.expenseUnknownSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseUnknownSupplierId. |
| `invoiceDetail.invoice.companyDTO.expenseSigningRule` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseSigningRule. |
| `invoiceDetail.invoice.companyDTO.requisitionNoApproval` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionNoApproval. |
| `invoiceDetail.invoice.companyDTO.ean` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Ean. |
| `invoiceDetail.invoice.companyDTO.purchaseRequisitionSetAccountOutstandingAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseRequisitionSetAccountOutstandingAmount. |
| `invoiceDetail.invoice.companyDTO.calculationChangedMatchedAmount` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculationChangedMatchedAmount. |
| `invoiceDetail.invoice.companyDTO.checkSumOfInvoiceLines` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckSumOfInvoiceLines. |
| `invoiceDetail.invoice.companyDTO.useBuyersHelp` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseBuyersHelp. |
| `invoiceDetail.invoice.companyDTO.expensePrivateAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpensePrivateAccountId. |
| `invoiceDetail.invoice.companyDTO.allocateDeviationTotalAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocateDeviationTotalAmount. |
| `invoiceDetail.invoice.companyDTO.requisitionTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.expenseAdvanceAsCredit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAdvanceAsCredit. |
| `invoiceDetail.invoice.companyDTO.objectType1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType1Name. |
| `invoiceDetail.invoice.companyDTO.objectType2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType2Name. |
| `invoiceDetail.invoice.companyDTO.objectType3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType3Name. |
| `invoiceDetail.invoice.companyDTO.objectType4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType4Name. |
| `invoiceDetail.invoice.companyDTO.objectType5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType5Name. |
| `invoiceDetail.invoice.companyDTO.objectType6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType6Name. |
| `invoiceDetail.invoice.companyDTO.objectType7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType7Name. |
| `invoiceDetail.invoice.companyDTO.objectType8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ObjectType8Name. |
| `invoiceDetail.invoice.companyDTO.checkAmountForCreditNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAmountForCreditNote. |
| `invoiceDetail.invoice.companyDTO.expenseVatfromMatch` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseVatfromMatch. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderDeliverySetDeliveryNote` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderDeliverySetDeliveryNote. |
| `invoiceDetail.invoice.companyDTO.checkDuplicateExpenses` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckDuplicateExpenses. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowAtUnknown` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowAtUnknown. |
| `invoiceDetail.invoice.companyDTO.expenditureFlowProposalIdatUnknown` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenditureFlowProposalIdatUnknown. |
| `invoiceDetail.invoice.companyDTO.acceptPartialDelivery` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AcceptPartialDelivery. |
| `invoiceDetail.invoice.companyDTO.requisitionSubjectRequired` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RequisitionSubjectRequired. |
| `invoiceDetail.invoice.companyDTO.alwaysCalculateVat` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceTwoRolesApproval` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.allowPostingToCostAccount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllowPostingToCostAccount. |
| `invoiceDetail.invoice.companyDTO.expenseInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseInvoiceSeries. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountPostingTwoRolesApproval` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountPostingTwoRolesApproval. |
| `invoiceDetail.invoice.companyDTO.deliveryCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO DeliveryCode. |
| `invoiceDetail.invoice.companyDTO.expenseAlwaysCalculateVat` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ExpenseAlwaysCalculateVat. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingLineNoSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingLineNoSetting. |
| `invoiceDetail.invoice.companyDTO.allocationSetting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AllocationSetting. |
| `invoiceDetail.invoice.companyDTO.calculateVatamountOnCostLine` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CalculateVatamountOnCostLine. |
| `invoiceDetail.invoice.companyDTO.compressPostingsDeliveredSeperately` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompressPostingsDeliveredSeperately. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference1Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference1Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingReference2Setting` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingReference2Setting. |
| `invoiceDetail.invoice.companyDTO.invoiceAccountCodingUseDefaultObjectSetting` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceAccountCodingUseDefaultObjectSetting. |
| `invoiceDetail.invoice.companyDTO.aiInvoice` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoice. |
| `invoiceDetail.invoice.companyDTO.aiInvoiceConfidenceTransfer` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiInvoiceConfidenceTransfer. |
| `invoiceDetail.invoice.companyDTO.arrivalAccountCodingUpdate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ArrivalAccountCodingUpdate. |
| `invoiceDetail.invoice.companyDTO.supplierMatchPattern` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO SupplierMatchPattern. |
| `invoiceDetail.invoice.companyDTO.vatObjectTypeNo2` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VatObjectTypeNo2. |
| `invoiceDetail.invoice.companyDTO.createDeliveryReturns` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CreateDeliveryReturns. |
| `invoiceDetail.invoice.companyDTO.flowAdditionCheckType` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO FlowAdditionCheckType. |
| `invoiceDetail.invoice.companyDTO.varianceVatAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO VarianceVatAccountId. |
| `invoiceDetail.invoice.companyDTO.maxVarianceAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO MaxVarianceAmount. |
| `invoiceDetail.invoice.companyDTO.aiNoPrediction` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO AiNoPrediction. |
| `invoiceDetail.invoice.companyDTO.useObjectRelationFilter` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseObjectRelationFilter. |
| `invoiceDetail.invoice.companyDTO.vat1AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat1AccountId. |
| `invoiceDetail.invoice.companyDTO.vat2AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat2AccountId. |
| `invoiceDetail.invoice.companyDTO.vat3AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat3AccountId. |
| `invoiceDetail.invoice.companyDTO.vat4AccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO Vat4AccountId. |
| `invoiceDetail.invoice.companyDTO.onlyApplyAlMatchingResult` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO OnlyApplyAlMatchingResult. |
| `invoiceDetail.invoice.companyDTO.useAutomaticPomatching` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAutomaticPomatching. |
| `invoiceDetail.invoice.companyDTO.purchaseOrderNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO PurchaseOrderNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.contractNoregexValidation` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO ContractNoregexValidation. |
| `invoiceDetail.invoice.companyDTO.rillionCaptureUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCaptureUrl. |
| `invoiceDetail.invoice.companyDTO.rillionCapturelabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RillionCapturelabel. |
| `invoiceDetail.invoice.companyDTO.eInvoiceUrl` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceUrl. |
| `invoiceDetail.invoice.companyDTO.eInvoiceLabel` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyDTO EInvoiceLabel. |
| `invoiceDetail.invoice.companyDTO.useAmountInRounding` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseAmountInRounding. |
| `invoiceDetail.invoice.companyDTO.roundingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO RoundingAmount. |
| `invoiceDetail.invoice.companyDTO.useInvoiceDateForExchangeRate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO UseInvoiceDateForExchangeRate. |
| `invoiceDetail.invoice.companyDTO.invoiceFlowDelaySetting` | body | `number` | yes | Request body value for InvoiceDetail Invoice CompanyDTO InvoiceFlowDelaySetting. |
| `invoiceDetail.invoice.companyDTO.checkAllocationStartDateClosedPeriod` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CheckAllocationStartDateClosedPeriod. |
| `invoiceDetail.invoice.companyDTO.companyAlias` | body | `array` | yes | Request body value for InvoiceDetail Invoice CompanyDTO CompanyAlias. |
| `invoiceDetail.invoice.companyName` | body | `string` | yes | Request body value for InvoiceDetail Invoice CompanyName. |
| `invoiceDetail.invoice.contractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ContractMatch. |
| `invoiceDetail.invoice.contractNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice ContractNo. |
| `invoiceDetail.invoice.crDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice CrDate. |
| `invoiceDetail.invoice.credit` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Credit. |
| `invoiceDetail.invoice.creditTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice CreditTime. |
| `invoiceDetail.invoice.currency` | body | `string` | yes | Request body value for InvoiceDetail Invoice Currency. |
| `invoiceDetail.invoice.currentLevel` | body | `number` | yes | Request body value for InvoiceDetail Invoice CurrentLevel. |
| `invoiceDetail.invoice.currentRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice CurrentRole. |
| `invoiceDetail.invoice.deptAccountId` | body | `number` | yes | Request body value for InvoiceDetail Invoice DeptAccountId. |
| `invoiceDetail.invoice.discountAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountAmount. |
| `invoiceDetail.invoice.discountDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DiscountDate. |
| `invoiceDetail.invoice.discountGrossAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice DiscountGrossAmount. |
| `invoiceDetail.invoice.discountPercentage` | body | `number` | yes | Request body value for InvoiceDetail Invoice DiscountPercentage. |
| `invoiceDetail.invoice.dueDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice DueDate. |
| `invoiceDetail.invoice.emailSignRole` | body | `string` | yes | Request body value for InvoiceDetail Invoice EmailSignRole. |
| `invoiceDetail.invoice.exchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExchangeRate. |
| `invoiceDetail.invoice.systemCurrencyExchangeRate` | body | `number` | yes | Request body value for InvoiceDetail Invoice SystemCurrencyExchangeRate. |
| `invoiceDetail.invoice.expenseMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExpenseMatch. |
| `invoiceDetail.invoice.extraAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice ExtraAmount. |
| `invoiceDetail.invoice.extraId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExtraId. |
| `invoiceDetail.invoice.feeAmount1` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount1. |
| `invoiceDetail.invoice.feeAmount2` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount2. |
| `invoiceDetail.invoice.feeAmount3` | body | `number` | yes | Request body value for InvoiceDetail Invoice FeeAmount3. |
| `invoiceDetail.invoice.fileTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FileTypeId. |
| `invoiceDetail.invoice.flowAddition` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowAddition. |
| `invoiceDetail.invoice.flowProposal` | body | `string` | yes | Request body value for InvoiceDetail Invoice FlowProposal. |
| `invoiceDetail.invoice.flowProposalId` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowProposalId. |
| `invoiceDetail.invoice.flowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice FlowStatus. |
| `invoiceDetail.invoice.forPartialPayment` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice ForPartialPayment. |
| `invoiceDetail.invoice.group1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group1. |
| `invoiceDetail.invoice.group2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group2. |
| `invoiceDetail.invoice.group3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group3. |
| `invoiceDetail.invoice.group4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group4. |
| `invoiceDetail.invoice.group5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group5. |
| `invoiceDetail.invoice.group6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Group6. |
| `invoiceDetail.invoice.investigate` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice Investigate. |
| `invoiceDetail.invoice.invoiceAccountCodingAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceAccountCodingAmount. |
| `invoiceDetail.invoice.invoiceDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice InvoiceDate. |
| `invoiceDetail.invoice.invoiceFlowId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowId. |
| `invoiceDetail.invoice.invoiceFlowStatus` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceFlowStatus. |
| `invoiceDetail.invoice.invoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceId. |
| `invoiceDetail.invoice.invoiceImageFileExtension` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceImageFileExtension. |
| `invoiceDetail.invoice.invoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice InvoiceNo. |
| `invoiceDetail.invoice.invoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceSeries. |
| `invoiceDetail.invoice.invoiceStatusMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice InvoiceStatusMessage. |
| `invoiceDetail.invoice.isContractMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsContractMatch. |
| `invoiceDetail.invoice.isPurchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice IsPurchaseOrderMatch. |
| `invoiceDetail.invoice.latestDiaryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNote. |
| `invoiceDetail.invoice.latestDiaryNoteUser` | body | `string` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteUser. |
| `invoiceDetail.invoice.latestDiaryNoteTime` | body | `date` | yes | Request body value for InvoiceDetail Invoice LatestDiaryNoteTime. |
| `invoiceDetail.invoice.linkedInvoiceId` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceId. |
| `invoiceDetail.invoice.linkedInvoiceNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceNo. |
| `invoiceDetail.invoice.linkedInvoiceSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice LinkedInvoiceSeries. |
| `invoiceDetail.invoice.matchedContractId` | body | `number` | yes | Request body value for InvoiceDetail Invoice MatchedContractId. |
| `invoiceDetail.invoice.netAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice NetAmount. |
| `invoiceDetail.invoice.noOfRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfRoles. |
| `invoiceDetail.invoice.object1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1. |
| `invoiceDetail.invoice.object1Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object1Id. |
| `invoiceDetail.invoice.object1Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object1Name. |
| `invoiceDetail.invoice.object2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2. |
| `invoiceDetail.invoice.object2Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object2Id. |
| `invoiceDetail.invoice.object2Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object2Name. |
| `invoiceDetail.invoice.object3` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3. |
| `invoiceDetail.invoice.object3Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object3Id. |
| `invoiceDetail.invoice.object3Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object3Name. |
| `invoiceDetail.invoice.object4` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4. |
| `invoiceDetail.invoice.object4Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object4Id. |
| `invoiceDetail.invoice.object4Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object4Name. |
| `invoiceDetail.invoice.object5` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5. |
| `invoiceDetail.invoice.object5Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object5Id. |
| `invoiceDetail.invoice.object5Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object5Name. |
| `invoiceDetail.invoice.object6` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6. |
| `invoiceDetail.invoice.object6Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object6Id. |
| `invoiceDetail.invoice.object6Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object6Name. |
| `invoiceDetail.invoice.object7` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7. |
| `invoiceDetail.invoice.object7Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object7Id. |
| `invoiceDetail.invoice.object7Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object7Name. |
| `invoiceDetail.invoice.object8` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8. |
| `invoiceDetail.invoice.object8Id` | body | `number` | yes | Request body value for InvoiceDetail Invoice Object8Id. |
| `invoiceDetail.invoice.object8Name` | body | `string` | yes | Request body value for InvoiceDetail Invoice Object8Name. |
| `invoiceDetail.invoice.oldAccountCodingDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice OldAccountCodingDate. |
| `invoiceDetail.invoice.originalSupplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierId. |
| `invoiceDetail.invoice.originalSupplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalSupplierName. |
| `invoiceDetail.invoice.originalVatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice OriginalVatType. |
| `invoiceDetail.invoice.partialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmount. |
| `invoiceDetail.invoice.partialPaymentAmountUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PartialPaymentAmountUpdated. |
| `invoiceDetail.invoice.paymentDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice PaymentDate. |
| `invoiceDetail.invoice.paymentMessage` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentMessage. |
| `invoiceDetail.invoice.paymentTerm` | body | `string` | yes | Request body value for InvoiceDetail Invoice PaymentTerm. |
| `invoiceDetail.invoice.paymentTermId` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTermId. |
| `invoiceDetail.invoice.paymentTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice PaymentTime. |
| `invoiceDetail.invoice.payReference` | body | `string` | yes | Request body value for InvoiceDetail Invoice PayReference. |
| `invoiceDetail.invoice.periodAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice PeriodAmount. |
| `invoiceDetail.invoice.postingsUpdated` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice PostingsUpdated. |
| `invoiceDetail.invoice.processDays` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessDays. |
| `invoiceDetail.invoice.processTime` | body | `number` | yes | Request body value for InvoiceDetail Invoice ProcessTime. |
| `invoiceDetail.invoice.purchaseOrderMatch` | body | `number` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderMatch. |
| `invoiceDetail.invoice.purchaseOrderNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice PurchaseOrderNo. |
| `invoiceDetail.invoice.reference1` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference1. |
| `invoiceDetail.invoice.reference2` | body | `string` | yes | Request body value for InvoiceDetail Invoice Reference2. |
| `invoiceDetail.invoice.remainingPartialPaymentAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice RemainingPartialPaymentAmount. |
| `invoiceDetail.invoice.reminderReason` | body | `number` | yes | Request body value for InvoiceDetail Invoice ReminderReason. |
| `invoiceDetail.invoice.role` | body | `string` | yes | Request body value for InvoiceDetail Invoice Role. |
| `invoiceDetail.invoice.showDate` | body | `date` | yes | Request body value for InvoiceDetail Invoice ShowDate. |
| `invoiceDetail.invoice.status` | body | `number` | yes | Request body value for InvoiceDetail Invoice Status. |
| `invoiceDetail.invoice.supplier` | body | `string` | yes | Request body value for InvoiceDetail Invoice Supplier. |
| `invoiceDetail.invoice.supplierActiveCreditCard` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice SupplierActiveCreditCard. |
| `invoiceDetail.invoice.supplierAddress1` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress1. |
| `invoiceDetail.invoice.supplierAddress2` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress2. |
| `invoiceDetail.invoice.supplierAddress3` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress3. |
| `invoiceDetail.invoice.supplierAddress4` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress4. |
| `invoiceDetail.invoice.supplierAddress5` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress5. |
| `invoiceDetail.invoice.supplierAddress6` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierAddress6. |
| `invoiceDetail.invoice.supplierBankAccount` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierBankAccount. |
| `invoiceDetail.invoice.supplierDeliveryNote` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierDeliveryNote. |
| `invoiceDetail.invoice.supplierId` | body | `number` | yes | Request body value for InvoiceDetail Invoice SupplierId. |
| `invoiceDetail.invoice.supplierInvoiceNo` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierInvoiceNo. |
| `invoiceDetail.invoice.supplierName` | body | `string` | yes | Request body value for InvoiceDetail Invoice SupplierName. |
| `invoiceDetail.invoice.noOfImages` | body | `number` | yes | Request body value for InvoiceDetail Invoice NoOfImages. |
| `invoiceDetail.invoice.timestamp` | body | `number` | yes | Request body value for InvoiceDetail Invoice Timestamp. |
| `invoiceDetail.invoice.type` | body | `number` | yes | Request body value for InvoiceDetail Invoice Type. |
| `invoiceDetail.invoice.updateSupplierOrAmount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UpdateSupplierOrAmount. |
| `invoiceDetail.invoice.useDiscount` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice UseDiscount. |
| `invoiceDetail.invoice.vatAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatAmount. |
| `invoiceDetail.invoice.vat1Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat1Amount. |
| `invoiceDetail.invoice.vat2Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat2Amount. |
| `invoiceDetail.invoice.vat3Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat3Amount. |
| `invoiceDetail.invoice.vat4Amount` | body | `number` | yes | Request body value for InvoiceDetail Invoice Vat4Amount. |
| `invoiceDetail.invoice.vatCalculation` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice VatCalculation. |
| `invoiceDetail.invoice.vatCode` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatCode. |
| `invoiceDetail.invoice.vatCodeID` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatCodeID. |
| `invoiceDetail.invoice.vatType` | body | `string` | yes | Request body value for InvoiceDetail Invoice VatType. |
| `invoiceDetail.invoice.vatTypeId` | body | `number` | yes | Request body value for InvoiceDetail Invoice VatTypeId. |
| `invoiceDetail.invoice.voucherNo` | body | `number` | yes | Request body value for InvoiceDetail Invoice VoucherNo. |
| `invoiceDetail.invoice.voucherSeries` | body | `string` | yes | Request body value for InvoiceDetail Invoice VoucherSeries. |
| `invoiceDetail.invoice.externalId` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalId. |
| `invoiceDetail.invoice.externalSource` | body | `string` | yes | Request body value for InvoiceDetail Invoice ExternalSource. |
| `invoiceDetail.invoice.isDynamicFlow` | body | `boolean` | yes | Request body value for InvoiceDetail Invoice IsDynamicFlow. |
| `invoiceDetail.invoice.authorizationAmountRequiredForNewFlowRoles` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountRequiredForNewFlowRoles. |
| `invoiceDetail.invoice.authorizationAmountData` | body | `object` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData. |
| `invoiceDetail.invoice.authorizationAmountData.generalAuthorizationAmount` | body | `number` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData GeneralAuthorizationAmount. |
| `invoiceDetail.invoice.authorizationAmountData.roleAuthorizationAmounts` | body | `array` | yes | Request body value for InvoiceDetail Invoice AuthorizationAmountData RoleAuthorizationAmounts. |
| `invoiceDetail.invoiceAccountCodings` | body | `array` | yes | Request body value for InvoiceDetail InvoiceAccountCodings. |
| `invoiceDetail.invoiceFlows` | body | `array` | yes | Request body value for InvoiceDetail InvoiceFlows. |
| `invoiceDetail.invoiceDiaries` | body | `array` | yes | Request body value for InvoiceDetail InvoiceDiaries. |
| `invoiceDetail.objectTypes` | body | `array` | yes | Request body value for InvoiceDetail ObjectTypes. |
