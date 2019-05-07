# ![LOGO](logo.png) cBioPortal web API [Beta] **flow**ground Connector

## Description

A generated **flow**ground connector for the cBioPortal web API [Beta] API (version 1.0 (beta)).

Generated from: http://www.cbioportal.org/api/api-docs<br/>
Generated at: 2019-05-07T17:39:51+03:00

## API Description

A web service for supplying JSON formatted data to cBioPortal clients. Please note that this API is currently in beta and subject to change.

## Authorization

This API does not require authorization.

## Actions

### Get all cancer types

*Tags:* `Cancer Types`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: cancerTypeId, name, clinicalTrialKeywords, dedicatedColor, shortName, parent.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get a cancer type

*Tags:* `Cancer Types`

#### Input Parameters
* `cancerTypeId` - _required_ - Cancer Type ID e.g. acc

### Get all clinical attributes

*Tags:* `Clinical Attributes`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: clinicalAttributeId, displayName, description, datatype, patientAttribute, priority, studyId.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get counts for clinical attributes according to their data availability for selected samples/patients

*Tags:* `Clinical Attributes`

### Fetch clinical attributes

*Tags:* `Clinical Attributes`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Fetch clinical data by patient IDs or sample IDs (all studies)

*Tags:* `Clinical Data`

#### Input Parameters
* `clinicalDataType` - _optional_ - Type of the clinical data
    Possible values: SAMPLE, PATIENT.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Fetch copy number segments by sample ID

*Tags:* `Copy Number Segments`

#### Input Parameters
* `chromosome` - _optional_ - Chromosome
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Fetch gene panel data

*Tags:* `Gene Panels`

### Get all gene panels

*Tags:* `Gene Panels`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: genePanelId, description.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get gene panel

*Tags:* `Gene Panels`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get gene panel

*Tags:* `Gene Panels`

#### Input Parameters
* `genePanelId` - _required_ - Gene Panel ID e.g. NSCLC_UNITO_2016_PANEL

### Get all genes

*Tags:* `Genes`

#### Input Parameters
* `keyword` - _optional_ - Search keyword that applies to hugo gene symbol of the genes
* `alias` - _optional_ - Alias of the gene
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: entrezGeneId, hugoGeneSymbol, type, cytoband, length.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch genes by ID

*Tags:* `Genes`

#### Input Parameters
* `geneIdType` - _optional_ - Type of gene ID
    Possible values: ENTREZ_GENE_ID, HUGO_GENE_SYMBOL.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get a gene

*Tags:* `Genes`

#### Input Parameters
* `geneId` - _required_ - Entrez Gene ID or Hugo Gene Symbol e.g. 1 or A1BG

### Get aliases of a gene

*Tags:* `Genes`

#### Input Parameters
* `geneId` - _required_ - Entrez Gene ID or Hugo Gene Symbol e.g. 1 or A1BG

### Fetch molecular data

*Tags:* `Molecular Data`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get all molecular profiles

*Tags:* `Molecular Profiles`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: molecularProfileId, molecularAlterationType, datatype, name, description, showProfileInAnalysisTab.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch molecular profiles

*Tags:* `Molecular Profiles`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get molecular profile

*Tags:* `Molecular Profiles`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_mutations

### Get discrete copy number alterations in a molecular profile

*Tags:* `Discrete Copy Number Alterations`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_gistic
* `sampleListId` - _required_ - Sample List ID e.g. acc_tcga_all
* `discreteCopyNumberEventType` - _optional_ - Type of the copy number event
    Possible values: HOMDEL_AND_AMP, HOMDEL, AMP, GAIN, HETLOSS, DIPLOID, ALL.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get counts of specific genes and alterations within a CNA molecular profile

*Tags:* `Discrete Copy Number Alterations`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_gistic

### Fetch discrete copy number alterations in a molecular profile by sample ID

*Tags:* `Discrete Copy Number Alterations`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_gistic
* `discreteCopyNumberEventType` - _optional_ - Type of the copy number event
    Possible values: HOMDEL_AND_AMP, HOMDEL, AMP, GAIN, HETLOSS, DIPLOID, ALL.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get gene panel data

*Tags:* `Gene Panels`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. nsclc_unito_2016_mutations

### Get all molecular data in a molecular profile

*Tags:* `Molecular Data`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_rna_seq_v2_mrna
* `sampleListId` - _required_ - Sample List ID e.g. acc_tcga_all
* `entrezGeneId` - _required_ - Entrez Gene ID e.g. 1
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Fetch molecular data in a molecular profile

*Tags:* `Molecular Data`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_rna_seq_v2_mrna
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get mutations in a molecular profile by Sample List ID

*Tags:* `Mutations`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_mutations
* `sampleListId` - _required_ - Sample List ID e.g. acc_tcga_all
* `entrezGeneId` - _optional_ - Entrez Gene ID
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: entrezGeneId, center, mutationStatus, validationStatus, tumorAltCount, tumorRefCount, normalAltCount, normalRefCount, aminoAcidChange, startPosition, endPosition, referenceAllele, variantAllele, proteinChange, mutationType, ncbiBuild, variantType, refseqMrnaId, proteinPosStart, proteinPosEnd, keyword.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch mutations in a molecular profile

*Tags:* `Mutations`

#### Input Parameters
* `molecularProfileId` - _required_ - Molecular Profile ID e.g. acc_tcga_mutations
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: entrezGeneId, center, mutationStatus, validationStatus, tumorAltCount, tumorRefCount, normalAltCount, normalRefCount, aminoAcidChange, startPosition, endPosition, referenceAllele, variantAllele, proteinChange, mutationType, ncbiBuild, variantType, refseqMrnaId, proteinPosStart, proteinPosEnd, keyword.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch mutation counts in all studies by gene and position

*Tags:* `Mutations`

### Fetch mutations in multiple molecular profiles by sample IDs

*Tags:* `Mutations`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: entrezGeneId, center, mutationStatus, validationStatus, tumorAltCount, tumorRefCount, normalAltCount, normalRefCount, aminoAcidChange, startPosition, endPosition, referenceAllele, variantAllele, proteinChange, mutationType, ncbiBuild, variantType, refseqMrnaId, proteinPosStart, proteinPosEnd, keyword.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all patients

*Tags:* `Patients`

#### Input Parameters
* `keyword` - _optional_ - Search keyword that applies to ID of the patients
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: patientId.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch patients by ID

*Tags:* `Patients`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get all sample lists

*Tags:* `Sample Lists`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: sampleListId, category, studyId, name, description.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch sample lists by ID

*Tags:* `Sample Lists`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get sample list

*Tags:* `Sample Lists`

#### Input Parameters
* `sampleListId` - _required_ - Sample List ID e.g. acc_tcga_all

### Get all sample IDs in a sample list

*Tags:* `Sample Lists`

#### Input Parameters
* `sampleListId` - _required_ - Sample List ID e.g. acc_tcga_all

### Fetch samples by ID

*Tags:* `Samples`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get all studies

*Tags:* `Studies`

#### Input Parameters
* `keyword` - _optional_ - Search keyword that applies to name and cancer type of the studies
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: studyId, cancerTypeId, name, shortName, description, publicStudy, pmid, citation, groups, status, importDate.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch studies by IDs

*Tags:* `Studies`

#### Input Parameters
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get the study tags by IDs

*Tags:* `Studies`

### Get a study

*Tags:* `Studies`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga

### Get all clinical attributes in the specified study

*Tags:* `Clinical Attributes`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: clinicalAttributeId, displayName, description, datatype, patientAttribute, priority, studyId.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get specified clinical attribute

*Tags:* `Clinical Attributes`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `clinicalAttributeId` - _required_ - Clinical Attribute ID e.g. CANCER_TYPE

### Get all clinical data in a study

*Tags:* `Clinical Data`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `attributeId` - _optional_ - Attribute ID e.g. CANCER_TYPE
* `clinicalDataType` - _optional_ - Type of the clinical data
    Possible values: SAMPLE, PATIENT.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: clinicalAttributeId, value.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Fetch clinical data by patient IDs or sample IDs (specific study)

*Tags:* `Clinical Data`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `clinicalDataType` - _optional_ - Type of the clinical data
    Possible values: SAMPLE, PATIENT.
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.

### Get all molecular profiles in a study

*Tags:* `Molecular Profiles`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: molecularProfileId, molecularAlterationType, datatype, name, description, showProfileInAnalysisTab.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all patients in a study

*Tags:* `Patients`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: patientId.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get a patient in a study

*Tags:* `Patients`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `patientId` - _required_ - Patient ID e.g. TCGA-OR-A5J2

### Get all clinical data of a patient in a study

*Tags:* `Clinical Data`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `patientId` - _required_ - Patient ID e.g. TCGA-OR-A5J2
* `attributeId` - _optional_ - Attribute ID e.g. AGE
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: clinicalAttributeId, value.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all clinical events of a patient in a study

*Tags:* `Clinical Events`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. lgg_ucsf_2014
* `patientId` - _required_ - Patient ID e.g. P01
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: eventType, startNumberOfDaysSinceDiagnosis, endNumberOfDaysSinceDiagnosis.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all samples of a patient in a study

*Tags:* `Samples`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `patientId` - _required_ - Patient ID e.g. TCGA-OR-A5J2
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: sampleId, sampleType.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all sample lists in a study

*Tags:* `Sample Lists`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: sampleListId, category, studyId, name, description.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get all samples in a study

*Tags:* `Samples`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: sampleId, sampleType.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get a sample in a study

*Tags:* `Samples`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `sampleId` - _required_ - Sample ID e.g. TCGA-OR-A5J2-01

### Get all clinical data of a sample in a study

*Tags:* `Clinical Data`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `sampleId` - _required_ - Sample ID e.g. TCGA-OR-A5J2-01
* `attributeId` - _optional_ - Attribute ID e.g. CANCER_TYPE
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: clinicalAttributeId, value.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get copy number segments in a sample in a study

*Tags:* `Copy Number Segments`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga
* `sampleId` - _required_ - Sample ID e.g. TCGA-OR-A5J2-01
* `chromosome` - _optional_ - Chromosome
* `projection` - _optional_ - Level of detail of the response
    Possible values: ID, SUMMARY, DETAILED, META.
* `pageSize` - _optional_ - Page size of the result list
* `pageNumber` - _optional_ - Page number of the result list
* `sortBy` - _optional_ - Name of the property that the result list is sorted by
    Possible values: chromosome, start, end, numberOfProbes, segmentMean.
* `direction` - _optional_ - Direction of the sort
    Possible values: ASC, DESC.

### Get the tags of a study

*Tags:* `Studies`

#### Input Parameters
* `studyId` - _required_ - Study ID e.g. acc_tcga

## License

**flow**ground :- Telekom iPaaS / c-bio-portal-web-api-beta-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
