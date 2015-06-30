+++
weight = "10"
type = "post"
draft = false
sidebar = true
Title = "IOOS Biological Observations Data Services"
date = 2014-08-04T07:56:39Z
+++

<!-- For a single homepage put in FrontMatter [url = "index.html"] -->


_The IOOS Biological Observations Data Services address the Data Management and Communications (DMAC) requirements that pertain to biological observations standards and interoperability applicable to U.S. IOOS and to various observing systems. Biological observations are highly heterogeneous and the variety of formats, logical structures, and sampling methods create significant challenges. 
The objective of the IOOS Biological Observations Services is to develop and deploy an efficient and effective information infrastructure for biological observations, adding components and links as necessary to serve end-users._
<!--more-->
 


# Biological Data Standards 

The IOOS Biological Observations Data Services had adopted/adapted or had built the following data standards:

* Schema Terminology will be based on ratified [Darwin core](http://rs.tdwg.org/dwc/), [Dublin core](http://dublincore.org/documents/dces/) and proposed IOOS vocabularies. XML guide will also based on Darwin core XML guidance.
* [CF Conventions](http://cfconventions.org/) had been applied to biological data definition at the field level. This is to assure that IOOS Biological Project will be compatible with other geophysical datasets.
* [FGDC Content Standard for Digital Geospatial Metadata (CSDGM)](http://www.fgdc.gov/metadata/geospatial-metadata-standards#csdgm) and [ISO 19115-2](http://service.ncddc.noaa.gov/rdn/www/metadata-standards/documents/MI-Metadata.pdf) are the adopted Metadata standards.
* [ERDDAP](http://coastwatch.pfeg.noaa.gov/erddap/index.html) is the main webservice for this project.
* [Environmental Data Connector (EDC)](http://www.pfeg.noaa.gov/products/EDC/) is the client developed to connect directly to ERDDAP and access data using customer application tools such as [ArcGIS](http://www.esri.com/software/arcgis) and [R Project](http://www.r-project.org/).
* To learn more about the biological data standards implemented at the Pacific Islands Region please follow the following links: 
  - [Biological data services at the Pacific Islands Region website](http://pacioos-mapserver2.ancl.hawaii.edu/erddap/info/index.html?page=1&itemsPerPage=1000)
  - [FGDC and ISO Metadata](http://oos.soest.hawaii.edu/cgi-bin/get_metadata.py?id=PACN_FISH_TRANSECT&format=fgdc)

<br>
<br>


# IOOS Biological Data Terminology

The IOOS Biological Data terminology is a list of data fields with names, descriptions, and format notes. It was based on ratified Darwin core, Dublin core and proposed IOOS vocabularies. XML guide was based on Darwin core XML guidance. CF Conventions had been applied to biological data definition at the field level. This is to assure that IOOS Biological Project will be compatible with other IOOS geophysical datasets. In order to “map” your database fields to the IOOS Biological Data terminology fields you will need to download the following files. 

## Version 1
 
* Originally submitted by Philip Goldstein, USGS/OBIS-USA on 2012-06-08
* [Marine Metadata Interoperability (MMI) Ontology Registry and Repository (ORR) Website](http://www.ioos.noaa.gov/exit.html?url=http%3A%2F%2Fmmisw.org%2Forr%2F%23http%3A%2F%2Fmmisw.org%2Font%2Fioos%2Fbiological).  The MMI ORR provides reference URLs that promote machine-to-machine discovery and use of ontologies and vocabularies.

### &nbsp; &nbsp; Definitions 

|	Term	|	Reference	|	Description
|	 ----------------------	|	 --------------------------	|	 --------------------------------------
|	modified	|	dcterms:modified	|	The most recent date the data originator updated or verified the record, expressed in the standard ISO 8601:2004(E). Can be the record creation date or date of subsequent update or verifiction. If the data originator does not record or provide this information, IOOS will populate this date with the date the record became available to IOOS.
|	verbatimModified	|	ioosbiology:verbatimModified	|	The date and time value of the "modified" term, recorded in the exact format that the data originator provided it, for purposes of audit trail, since IOOS will convert this to ISO 8601:2004(E) for operational purposes.
|	datasetID	|	dwc:datasetID	|	An abbreviated name for the dataset that contains this occurrence record. This may also be the technical name for the data resource in a database or web service. The datasetID occurs on each row to preserve record identity in case records served by the resource become distributed to other resources or applications.
|	datasetName	|	dwc:datasetName	|	This is a long-form name for the dataset, more explanatory than the datasetID. The datasetName will read as a recognizable title that reflects information about the dataset. Suggested information to include in the datasetName can refer to originator, content, purpose, method, geography, or other characteristics of the dataset. This datasetName term in the data record will match the dataset name in metadata.
|	higherInstitutionCode	|	ioosbiology:higherInstitutionCode	|	Institution codes, in the form of names, abbreviation or acronyms, separated by semicolons, that define the hierarchy of institutions within which the data originator operates. Includes the originating institution as the lowest level (rightmost) code. All abbreviations or acronyms for institutions in all levels of the hierarchy will be explained in dataset metadata. 
|	institutionCode	|	dwc:institutionCode	|	A name, abbreviation or acronym for the institution that is the originator of this data resource: the institution most directly involved in research, operations, data collection and/or data management that produced this dataset. This institution also appears as the lowest level (rightmost) code in the higherInstitutionCode term.
|	ownerInstitutionCode	|	ioosbiology:ownerInstitutionCode	|	An abbreviation that identifies the institution, within the "higherInstitutionCode" hierarchy, that is considered the owner or controller of the data.
|	collectionCode	|	dwc:collectionCode	|	An identifier for a subset(s) of data within the dataset, partitioned by methods or parameters meaningful to the data originators. The scheme and purpose for defining and partitioning by collectionCode within a dataset will be explained in metadata.
|	catalogNumber	|	dwc:catalogNumber	|	A record identifier provided by the data originator. The identifier is controlled by the data originator and reflects the originator's practices of data administration. Special concerns about the identifier, such as whether it is unique, if it is persistent, or if it contains embedded information, can be addressed in metadata if applicable.
|	observationDateTime	|	dwc:eventDate	|	The date and time of observation expressed in local time using the standard ISO 8601:2004(E). Where date and time are imprecise, for example, time not recorded or day not recorded, ISO 8601 practice is to omit the components of the date and time string for those unspecified details. Where date and time imprecision are more complex, for example, "observed between 10am and noon" or "observed during the first half of July", supplement the use of ISO 8601 in this term with the use of verbatimObservationDateTime, nominalObservationDateTime, nominalObservationDateTimeUncertainty, and observationDateTimeAnnotation.
|	observationTimeZone	|	ioosbiology:observationTimeZone	|	The time zone of the observation event, expressed as +/- hh:mm offset from UTC. While time zone information can also be included in the full ISO 8601 expression in observationDateTime, time zone is stored here for reliable use in nominalObservationDateTime and nominalObservationDateTimeUncertainty calculations. nominalObservationDateTime must be expressed in UTC.
|	observationDateTimeAnnotation	|	ioosbiology:observationDateTimeAnnotation	|	observationDateTimeAnnotation explains information about date and time that may not be evident in verbatim, ISO 8601, or nominal forms of the date and time. For example, date and time may include uncertainty, such as time of day left null because time was not recorded. Howewver, data originators may be able to say that although time was not recorded, the observation is known to have been made between 8am and 5pm local time. observationDateTimeAnnotation can provide a concise explanation of this condition. observationDateTimeAnnotation can also provide explanation for how nominalObservationDateTimeUncertainty was determined.
|	verbatimObservationDateTime	|	dwc:verbatimEventDate	|	The expression of the date and time of the observation in language identical to the originator's description of the date and time of observation. If the originator used a non-standard format or descriptive language for date and time, verbatimObservationDateTime contains this information.
|	nominalObservationDateTime	|	ioosbiology:nominalObservationDateTime	|	In an IOOS service, this variable may appear simply with the name "time" or with the full name "nominalObservationDateTime". This term identifies a specific instant chosen to represent the date and time of the observation, in Coordinated Universal Time (UTC). Both date and time are specified in this term in order to facilitate some searches and services that require resolution of events to this level of precision in time. Some observation events occur with uncertainty at the level of minutes, hours, or even days or more. A nominal event date and time is determined, even for observations with date and time uncertainty, for IOOS services to best represent the instant of the event. The companion term, nominalObservationDateTimeUncertainty, defines an interval of uncertainty that quantifies precision to correspond to the precision the original data recorded. Methods for determining nominal time and uncertainty will be documented in metadata, and they can be concisely explained in the "obsrvationDateTimeAnnotation" term.
|	nominalObservationDateTimeUncertainty	|	ioosbiology:nominalObservationDateTimeUncertainty	|	In an IOOS service, this variable may appear simply with the name "timeUncertainty" or with the full name "nominalObservationDateTimeUncertainty". This is the uncertainty in seconds before and after the nominalObservationDateTime, as a result of both precision and accuracy factors in determining observation time. This use of uncertainty makes the nominalObservationDateTime the mid-point in the range of uncertainty equal to twice the value of this term.
|	latitude	|	dwc:decimalLatitude	|	The position of the observation north or south of the equator in decimal degrees. Latitudes north of the equator are positive and range to +90 degrees. Positions south of the equator are negative, and range to -90 degrees.
|	longitude	|	dwc:decimalLongitude	|	The position of the observation east or west of the prime meridian in decimal degrees. Positions west of the prime meridian are negative, and range to -180. Positions east of the prime meridian are positive, and range to +180.
|	coordinateUncertaintyInMeters	|	dwc:coordinateUncertaintyInMeters	|	An expression in meters of the overall uncertainty of the georeference provided by the latitude and longitude data. The uncertainty can combine issues of both accuracy and precision, and depends on the method the data originator used to determine coordinates. Methods and considerations that go into determinations of uncertainty will be described in metadata.
|	geodeticDatum	|	dwc:geodeticDatum	|	The ellipsoid, geodetic datum, or spatial reference system used in decimalLatitude and decimalLongitude. IOOS preference is to provide all coordinates using EPSG:4326, also known as WGS 84. This element will identify the actual datum used, confirming WGS 84 or identifying what other datum applies.
|	georeferencedBy	|	dwc:georeferencedBy	|	The name or other identifier of individual(s) or institution(s) that determined the georeference. Can be a list delimited by semicolon.
|	georeferenceProtocol	|	dwc:georeferenceProtocol	|	A description or reference to the methods used to determine the spatial footprint, coordinates, and uncertainties.
|	verbatimCoordinates	|	dwc:verbatimCoordinates	|	Record original coordinate information here (both latitude and longitude) for audit trail purposes where necessary.
|	verbatimCoordinateSystem	|	dwc:verbatimCoordinateSystem	|	The spatial coordinate system for the verbatimLatitude and verbatimLongitude or the verbatimCoordinates.
|	verbatimSRS	|	dwc:verbatimSRS	|	The ellipsoid, geodetic datum, or spatial reference system (SRS) upon which coordinates given in verbatimCoordinates are based.
|	minimumDepthInMeters	|	dwc:minimumDepthInMeters	|	The minimumDepthInMeters and maximumDepthInMeters express the depth range in which the observation was made. If the data originator provides a single depth measurement, the minimumDepthInMeters and maximumDepthInMeters show that measurement and will be equal. If no depth information is provided, both the min and max terms will be NULL.
|	maximumDepthInMeters	|	dwc:maximumDepthInMeters	|	The minimumDepthInMeters and maximumDepthInMeters express the depth range in which the observation was made. If the data originator provides a single depth measurement, the minimumDepthInMeters and maximumDepthInMeters show that measurement and will be equal. If no depth information is provided, both the min and max terms will be NULL.
|	basisOfRecord	|	dwc:basisOfRecord	|	Identifies the source of information or observation that generated the biological occurrence record.
|	recordedBy	|	dwc:recordedBy	|	The name or other identifier of individual(s) or institution(s) responsible for making the observation and recording it in electronic form. Can be a list delimited by semicolon.
|	vernacularName	|	dwc:vernacularName	|	A common or vernacular name for the taxon observed. A vernacularName is not required. Use of this term is at the discretion of the data originator. If this term is used, then authorities, references and procedures for making identifications and translating vernacular name to scientific name should be documented in metadata. The recommended practice is that vernacular names be used consistently within a dataset.
|	scientificName	|	dwc:scientificName	|	The taxonomic identification of the observation as either 1) Genus and species (and subspecies if provided) in Latin binomial nomenclature form, or 2) the lowest-level taxonomic name to which the observation is identified, expressed in Latin form. scientificName is a required term. Authorities, references and procedures for making identifications should be documented in metadata.
|	taxonRank	|	dwc:taxonRank	|	The taxonRank term is a companion to the scientificName term. taxonRank identifies the taxonomic level of the lowest-level name in the scientificName term.
|	aphiaID	|	ioosbiology:aphiaID	|	A unique taxon identifier obtained by validation of the taxon name with the World Register of Marine Species (WoRMS), www.marinespecies.org.
|	tsn	|	ioosbiology:tsn	|	A unique taxon identifier obtained by validation of the taxon name with the Integrated Taxonomic Information System (ITIS), www.itis.gov.
|	individualCount	|	dwc:individualCount	|	The number of individuals represented in the observation record. Valid values include positive integers, zero, and null. Positive integers represent presence. If the observation record and metadata also contain other required information such as details about the sampling activity, individualCount can contribute to the abundance calculations. Null value for individualCount represents a record of presence, with quantity unspecified, and null values do not support abundance calculations. Zero value represents absence. Zero values for absence are only valid if methodology for establishing absence is recorded in metadata.
|	sex	|	dwc:sex	|	The sex of biological individuals represented in the observation record. Vocabulary will be consistent within a dataset and will be explained in metadata. Methods of determination (where applicable) will be explained in metadata.
|	lifeStage	|	dwc:lifeStage	|	An expression or description of age or lifestage of biological individual(s) in the observation record. Vocabulary will be consistent within a dataset and will be explained in metadata. Methods of determination (where applicable) will be explained in metadata.
|	observedIndividualLengthInCm	|	ioosbiology:observedIndividualLengthInCm	|	If a single individual is observed and measured, record length in centimeters here.
|	observedMeanLengthInCm	|	ioosbiology:observedMeanLengthInCm	|	If measuring more than one individual for aggregate length values, record mean length in centimeters here.
|	observedMaxLengthInCm	|	ioosbiology:observedMaxLengthInCm	|	If measuring more than one individual for aggregate length values, record maximum length in centimeters here.
|	observedMinLengthInCm	|	ioosbiology:observedMinLengthInCm	|	If measuring more than one individual for aggregate length values, record minimum length in centimeters here.
|	lengthType	|	ioosbiology:lengthType	|	The type or method of length measurement used in this observation record, such as TL for total length, FL for fork length, SL for standard length.
|	sampleID	|	ioosbiology:sampleID	|	A unique identifier for a unit of material that serves as a sample for a survey of biological occurrence (presence, absence or derived value). The definition of a sample and assignment of IDs is cojntroled by the data originator. If applicable, details about how sample ares are defined and IDs assigned will be provided in metadata.
|	subsampleID	|	ioosbiology:subsampleID	|	If a sample is further divided by the data originator for purposes of organization, handling or analysis, and if the data originator wants to maintain the identity of the subsample, capture the ID of the subsample here. Explain in metadata if applicable.
|	samplingProtocol	|	dwc:samplingProtocol	|	Information about the sampling method as defined by the data originator. Valid values include S for stationary, T for towed, D for diver swim. Contents or vacabulary used in this term will be used consistently in a dataset and will be explained in metadata. Additional information can be concatenated into the term, delimited by semicolon. More extensive discussion of sampling protocol, effort and conditions may be provided in metadata as needed.
|	samplingEffort	|	dwc:samplingEffort	|	Information about the extent, duration or other variable aspects of the sampling activity, as conducted by the data originator, that occurred at the time of the sampling event. More than one type of effort information can be concatenated into this term, delimited by semicolon. Other terms are available in this terminology for some specific details of sampling effort, such as sample dimensions, that are expected to be frequently used in IOOS services. Use the samplingEffort term for additional effort information that is not addressed by other terms. More extensive discussion of sampling protocol, effort and conditions may be provided in metadata as needed.
|	samplingConditions	|	ioosbiology:samplingConditions	|	Information about the state of the sampling location, determined by external factors such as weather, at the time of the sampling event. More than one type of information about conditions can be concatenated into this term, delimited by semicolon. Other terms are available in this terminology for some specific details of sampling conditions, such as habitat, bottomType, visibilty and temperature, that are expected to be frequently used in IOOS services. Use the samplingConditions term for additional information about conditions that is not addressed by other terms. More extensive discussion of sampling protocol, effort and conditions may be provided in metadata as needed.
|	sampleShape	|	ioosbiology:sampleShape	|	The shape of the sample space in which the observation was made, such as R for rectangular, C for cylindrical.
|	sampleWidthInMeters	|	ioosbiology:sampleWidthInMeters	|	The width in meters of the sample space in which the observation was made.
|	sampleHeightInMeters	|	ioosbiology:sampleHeightInMeters	|	The length in meters of the sample space in which the observation was made.
|	sampleRadiusInMeters	|	ioosbiology:sampleRadiusInMeters	|	The radius in meters of a cylindrical sample space.
|	sampleAreaInSquareMeters	|	ioosbiology:sampleAreaInSquareMeters	|	The area in square meters, if projected vertically to a plane representing the ocean surface, of the sample space in which the observation was made.
|	sampleVolumeInCubicMeters	|	ioosbiology:sampleVolumeInCubicMeters	|	The volume in cubic meters of the sample space in which the observation was made.
|	visibilityInMeters	|	ioosbiology:visibilityInMeters	|	Visibility through the water column in meters.
|	visibilityType	|	ioosbiology:visibilityType	|	The direction of estimated visibility, horizontal or vertical.
|	waterTemperatureInCelsius	|	ioosbiology:waterTemperatureInCelsius	|	The temperature of the water at the time of the observation, expressed in degrees Celsius.
|	habitat	|	dwc:habitat	|	A description or identifier of general information about the habitat in which the observation was made. Vocabulary will be consistent within a dataset and will be explained in metadata. Methods of determination (where applicable) will be explained in metadata.
|	bottomType	|	ioosbiology:bottomType	|	A description or identifier of general information about the sea floor at the coordinates or locality where the observation was made. Vocabulary will be consistent within a dataset and will be explained in metadata. Methods of determination (where applicable) will be explained in metadata.
|	quantificationVocabulary	|	ioosbiology:quantificationVocabulary	|	The names for dervied values, referred to as "quantification", can be drawn from a controlled vocabulary or vocabularies of quantification names. Or they can be reported in IOOS services using the verbatim name given by the data originator. Either the name of a controlled vocabulary or the word "verbatim" should be used in this term. Either way, within a dataset, both verbatim and vocabulary names must be used consistently, and explained in metadata.
|	quantificationName	|	dwc:measurementType	|	A name for a derived value or processed data about the occurrence, for example, "Biomass". The word used in this terminology for such information is "quantification", rather than "abundance", because "abundance" may have specific methodological immplications in biology. In this example, biomass would not be obtained at survey time, rather biomass would be calculated from input data that was obtained at survey time, combined with a biomass calculation methodology. This term is used along with companion terms for quantification value, units, uncertainty, method, and determination details. It is suggested that names for derived values be more specific than "Biomass", because many institutions will develop biomass information using diverse methods. Suggested practice is to include some more specific reference(s) in the quantification name, such as insitution, survey, date or other specifics. For example, "Biomass-PIFSC-2011", and explain naming in metadata. 
|	quantificationValue	|	dwc:measurementValue	|	The value of the derived information product, such as the numerical value for biomass. This term does not include units. Units are contained in another term.
|	quantificationUnit	|	dwc:measurementUnit	|	The units in which the value expresses the quantification, for example, "kg/m^2 surface" or "kilograms per square meter of ocean surface".
|	quantificationUncertainty	|	dwc:measurementAccuracy	|	An estimate of the uncertainty, positive or negative (+/-) offset of the stated value, that expresses the uncertainty of the value as calculated and reported. Note that the expression in this term can combine both accuracy and precision considerations to a more general estimate, uncertainty, hence the slightly different name for this term from compared to the Darwin Core (dwc) reference term.
|	quantificationDeterminedDate	|	dwc:measurementDeterminedDate	|	The date the quantification was determined. Can be different from the observation date.
|	quantificationDeterminedBy	|	dwc:measurementDeterminedBy	|	The name or ID of person(s) or institution(s) that determined the quantification.
|	quantificationMethod	|	dwc:measurementMethod	|	A reference to the method used to determine the quantification. This will be different from the method used to make the observation of biological occurrence; it will be the companion calucation method that followed the observation method. Quantification information is expected to be only useful if method is sufficiently documented, so this term is vitally important for use of quantification terms for derived values. This term can contain a code or other abbreviated reference to a method. In all cases quantificationMethod should be explained in metadata and supporting publications or related resources identified.
|	waterBody	|	dwc:waterBody	|	The name of the water body in which the observation was made. For marine data, this is the ocean name. If there is a more specific named region, such as a bay or reef, or sector of the ocean (for example, northwest Pacific), add the regional name after the ocean name, separated by a semicolon. Note that the locality term will contain the most specific name, such as a pier or other named feature, so that lowest level of detail is not included in waterbody. The waterbody term is for the ocean and any named intermediate geography such as a region.
|	islandGroup	|	dwc:islandGroup	|	The name of an island group associated with the location where the observation was made.
|	island	|	dwc:island	|	The name an island associated with the location where the observation was made.
|	locality	|	dwc:locality	|	The locality is the most specific named place to identify the location of the observation. Many marine data rely strictly on geographic coordinates, so the locality term may be null. If a locality is used, it may be a specific location or feature name, such as "Pier 39" or "Atafu Atoll", or it may be a descriptive phrase, such as "a tidal pool 1500 meters north of Pier 39". Note that in marine observations, the latitude and longitude may be more precise than any named place would suggest, because the coordinates often come from navigation of GPS systems. Place names can be secondary locality identifiers and thus less precise than coordinates.
|	country	|	dwc:country	|	The name of the country in which the observation location ocurs.
|	stateProvince	|	dwc:stateProvince	|	The name of the state or province in which the observation location ocurs. Such geographic named locations may not be available or applicable for marine data, and acordingly the use of this term is optional. In some cases such jurisdiction identification may be crucial for data attribution, management and/or use, so this term is retained in the terminology for cases where it may be essential.
|	county	|	dwc:county	|	The name of the county or other comparable geographic unit in which the observation location ocurs. Such geographic named locations may not be available or applicable for marine data, and acordingly the use of this term is optional. In some cases such jurisdiction identification may be crucial for data attribution, management and/or use, so this term is retained in the terminology for cases where it may be essential.
|	municipality	|	dwc:municipality	|	The name of the municipality in which the observation location ocurs. Such geographic named locations may not be available or applicable for marine data, and acordingly the use of this term is optional. In some cases such jurisdiction identification may be crucial for data attribution, management and/or use, so this term is retained in the terminology for cases where it may be essential.
|	geodeticDatum	|	dwc:geodeticDatum	|	The ellipsoid, geodetic datum, or spatial reference system used in decimalLatitude and decimalLongitude. IOOS preference is to provide all coordinates using EPSG:4326, also known as WGS 84. This element will identify the actual datum used, confirming WGS 84 or identifying what other datum applies.
|	kingdom	|	dwc:kingdom	|	The full scientific name of the kingdom in which the taxon is classified.
|	phylum	|	dwc:phylum	|	The full scientific name of the phylum in which the taxon is classified.
|	class	|	dwc:class	|	The full scientific name of the class in which the taxon is classified.
|	order	|	dwc:order	|	The full scientific name of the order in which the taxon is classified.
|	family	|	dwc:family	|	The full scientific name of the family in which the taxon is classified.
|	genus	|	dwc:genus	|	The full scientific name of the genus in which the taxon is classified.
|	subgenus	|	dwc:subgenus	|	The full scientific name of the subgenus in which the taxon is classified. Values should include the genus to avoid homonym confusion.
|	species	|	dwc:specificEpithet	|	The full scientific name of the species in which the taxon is classified. If a subspecies identification is provided, add the subspecies name after the species name separated by a space.
|	infraspecificEpithet	|	dwc:infraspecificEpithet	|	The full scientific name of the subspecies, variant or other finer level identification.
|	scientificNameAuthorship	|	dwc:scientificNameAuthorship	|	The authorship information for the scientificName.
|	taxonRemarks	|	dwc:taxonRemarks	|	Comments or notes about the taxon or name.
|	identifiedBy	|	dwc:identifiedBy	|	The name or other identifier of individual(s) or institution(s) that assigned the taxonomic name. Can be a list delimited by semicolon.
|	identificationDate	|	dwc:eventDate	|	The date the identification on this record was made, expressed in ISO 8601 date format.
|	identificationQualifier	|	dwc:identificationQualifier	|	A brief phrase or a standard term ("cf.", "aff.") to express the determiner's doubts about the Identification.
|	identificationRemarks	|	dwc:identificationRemarks	|	Comments or notes about the identification.

### &nbsp; &nbsp; Schema (XSD)

```
<?xml version="1.0"?>
<!-- version 0.9 2011/11/30 Philip Goldstein (University of Colorado, Boulder)
-->
<?xml-stylesheet href='ioosxsdstyle.xsl' type='text/xsl'?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:dwc="http://rs.tdwg.org/dwc/terms/"
    xmlns:dcterms="http://purl.org/dc/terms/" xmlns:ioosbiology="http://domain.gov/folder/terms/"
    targetNamespace="http://domain.gov/folder/terms/">

    <!--  Administration and identification terms  -->

    <xsd:element name="modified" ref="dcterms:modified" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The most recent date the data originator updated or verified the
                record, expressed in the standard ISO 8601:2004(E). Can be the record creation date
                or date of subsequent update or verifiction. If the data originator does not record
                or provide this information, IOOS will populate this date with the date the record
                became available to IOOS.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="verbatimModified" ref="ioosbiology:verbatimModified" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The date and time value of the "modified" term, recorded in the exact
                format that the data originator provided it, for purposes of audit trail, since IOOS
                will convert this to ISO 8601:2004(E) for operational purposes.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="datasetID" ref="dwc:datasetID" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>An abbreviated name for the dataset that contains this occurrence
                record. This may also be the technical name for the data resource in a database or
                web service. The datasetID occurs on each row to preserve record identity in case
                records served by the resource become distributed to other resources or
                applications.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="datasetName" ref="dwc:datasetName" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>This is a long-form name for the dataset, more explanatory than the
                datasetID. The datasetName will read as a recognizable title that reflects
                information about the dataset. Suggested information to include in the datasetName
                can refer to originator, content, purpose, method, geography, or other
                characteristics of the dataset. This datasetName term in the data record will match
                the dataset name in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="higherInstitutionCode" ref="ioosbiology:higherInstitutionCode"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Institution codes, in the form of names, abbreviation or acronyms,
                separated by semicolons, that define the hierarchy of institutions within which the
                data originator operates. Includes the originating institution as the lowest level
                (rightmost) code. All abbreviations or acronyms for institutions in all levels of
                the hierarchy will be explained in dataset metadata. </xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="institutionCode" ref="dwc:institutionCode" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A name, abbreviation or acronym for the institution that is the
                originator of this data resource: the institution most directly involved in
                research, operations, data collection and/or data management that produced this
                dataset. This institution also appears as the lowest level (rightmost) code in the
                higherInstitutionCode term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="ownerInstitutionCode" ref="ioosbiology:ownerInstitutionCode"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>An abbreviation that identifies the institution, within the
                "higherInstitutionCode" hierarchy, that is considered the owner or controller of the
                data.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="collectionCode" ref="dwc:collectionCode" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>An identifier for a subset(s) of data within the dataset, partitioned
                by methods or parameters meaningful to the data originators. The scheme and purpose
                for defining and partitioning by collectionCode within a dataset will be explained
                in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="catalogNumber" ref="dwc:catalogNumber" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A record identifier provided by the data originator. The identifier
                is controlled by the data originator and reflects the originator's practices of data
                administration. Special concerns about the identifier, such as whether it is unique,
                if it is persistent, or if it contains embedded information, can be addressed in
                metadata if applicable.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Date and time terms  -->

    <xsd:element name="observationDateTime" ref="dwc:eventDate" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The date and time of observation expressed in local time using the
                standard ISO 8601:2004(E). Where date and time are imprecise, for example, time not
                recorded or day not recorded, ISO 8601 practice is to omit the components of the
                date and time string for those unspecified details. Where date and time imprecision
                are more complex, for example, "observed between 10am and noon" or "observed during
                the first half of July", supplement the use of ISO 8601 in this term with the use of
                verbatimObservationDateTime, nominalObservationDateTime,
                nominalObservationDateTimeUncertainty, and
                observationDateTimeAnnotation.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observationTimeZone" ref="ioosbiology:observationTimeZone" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The time zone of the observation event, expressed as +/- hh:mm offset
                from UTC. While time zone information can also be included in the full ISO 8601
                expression in observationDateTime, time zone is stored here for reliable use in
                nominalObservationDateTime and nominalObservationDateTimeUncertainty calculations.
                nominalObservationDateTime must be expressed in UTC.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observationDateTimeAnnotation"
        ref="ioosbiology:observationDateTimeAnnotation" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>observationDateTimeAnnotation explains information about date and
                time that may not be evident in verbatim, ISO 8601, or nominal forms of the date and
                time. For example, date and time may include uncertainty, such as time of day left
                null because time was not recorded. Howewver, data originators may be able to say
                that although time was not recorded, the observation is known to have been made
                between 8am and 5pm local time. observationDateTimeAnnotation can provide a concise
                explanation of this condition. observationDateTimeAnnotation can also provide
                explanation for how nominalObservationDateTimeUncertainty was
                determined.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="verbatimObservationDateTime" ref="dwc:verbatimEventDate" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The expression of the date and time of the observation in language
                identical to the originator's description of the date and time of observation. If
                the originator used a non-standard format or descriptive language for date and time,
                verbatimObservationDateTime contains this information.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="nominalObservationDateTime" ref="ioosbiology:nominalObservationDateTime"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>In an IOOS service, this variable may appear simply with the name
                "time" or with the full name "nominalObservationDateTime". This term identifies a
                specific instant chosen to represent the date and time of the observation, in
                Coordinated Universal Time (UTC). Both date and time are specified in this term in
                order to facilitate some searches and services that require resolution of events to
                this level of precision in time. Some observation events occur with uncertainty at
                the level of minutes, hours, or even days or more. A nominal event date and time is
                determined, even for observations with date and time uncertainty, for IOOS services
                to best represent the instant of the event. The companion term,
                nominalObservationDateTimeUncertainty, defines an interval of uncertainty that
                quantifies precision to correspond to the precision the original data recorded.
                Methods for determining nominal time and uncertainty will be documented in metadata,
                and they can be concisely explained in the "obsrvationDateTimeAnnotation"
                term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="nominalObservationDateTimeUncertainty"
        ref="ioosbiology:nominalObservationDateTimeUncertainty" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>In an IOOS service, this variable may appear simply with the name
                "timeUncertainty" or with the full name "nominalObservationDateTimeUncertainty".
                This is the uncertainty in seconds before and after the nominalObservationDateTime,
                as a result of both precision and accuracy factors in determining observation time.
                This use of uncertainty makes the nominalObservationDateTime the mid-point in the
                range of uncertainty equal to twice the value of this term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Georeference (coordinate geography) terms  -->

    <xsd:element name="latitude" ref="dwc:decimalLatitude" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The position of the observation north or south of the equator in
                decimal degrees. Latitudes north of the equator are positive and range to +90
                degrees. Positions south of the equator are negative, and range to -90
                degrees.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="longitude" ref="dwc:decimalLongitude" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The position of the observation east or west of the prime meridian in
                decimal degrees. Positions west of the prime meridian are negative, and range to
                -180. Positions east of the prime meridian are positive, and range to
                +180.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="coordinateUncertaintyInMeters" ref="dwc:coordinateUncertaintyInMeters"
        type="xsd:decimal">
        <xsd:annotation>
            <xsd:documentation>An expression in meters of the overall uncertainty of the
                georeference provided by the latitude and longitude data. The uncertainty can
                combine issues of both accuracy and precision, and depends on the method the data
                originator used to determine coordinates. Methods and considerations that go into
                determinations of uncertainty will be described in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="geodeticDatum" ref="dwc:geodeticDatum" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The ellipsoid, geodetic datum, or spatial reference system used in
                decimalLatitude and decimalLongitude. IOOS preference is to provide all coordinates
                using EPSG:4326, also known as WGS 84. This element will identify the actual datum
                used, confirming WGS 84 or identifying what other datum applies.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="georeferencedBy" ref="dwc:georeferencedBy" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name or other identifier of individual(s) or institution(s) that
                determined the georeference. Can be a list delimited by
                semicolon.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="georeferenceProtocol" ref="dwc:georeferenceProtocol" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A description or reference to the methods used to determine the
                spatial footprint, coordinates, and uncertainties.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="verbatimCoordinates" ref="dwc:verbatimCoordinates" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Record original coordinate information here (both latitude and
                longitude) for audit trail purposes where necessary.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="verbatimCoordinateSystem" ref="dwc:verbatimCoordinateSystem"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The spatial coordinate system for the verbatimLatitude and
                verbatimLongitude or the verbatimCoordinates.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="verbatimSRS" ref="dwc:verbatimSRS" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The ellipsoid, geodetic datum, or spatial reference system (SRS) upon
                which coordinates given in verbatimCoordinates are based.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Depth terms  -->

    <xsd:element name="minimumDepthInMeters" ref="dwc:minimumDepthInMeters" type="xsd:decimal">
        <xsd:annotation>
            <xsd:documentation>The minimumDepthInMeters and maximumDepthInMeters express the depth
                range in which the observation was made. If the data originator provides a single
                depth measurement, the minimumDepthInMeters and maximumDepthInMeters show that
                measurement and will be equal. If no depth information is provided, both the min and
                max terms will be NULL.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="maximumDepthInMeters" ref="dwc:maximumDepthInMeters" type="xsd:decimal">
        <xsd:annotation>
            <xsd:documentation>The minimumDepthInMeters and maximumDepthInMeters express the depth
                range in which the observation was made. If the data originator provides a single
                depth measurement, the minimumDepthInMeters and maximumDepthInMeters show that
                measurement and will be equal. If no depth information is provided, both the min and
                max terms will be NULL.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Record origination terms  -->

    <xsd:element name="basisOfRecord" ref="dwc:basisOfRecord" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Identifies the source of information or observation that generated
                the biological occurrence record.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="recordedBy" ref="dwc:recordedBy" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name or other identifier of individual(s) or institution(s)
                responsible for making the observation and recording it in electronic form. Can be a
                list delimited by semicolon.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Taxonomic identification terms  -->

    <xsd:element name="vernacularName" ref="dwc:vernacularName" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A common or vernacular name for the taxon observed. A vernacularName
                is not required. Use of this term is at the discretion of the data originator. If
                this term is used, then authorities, references and procedures for making
                identifications and translating vernacular name to scientific name should be
                documented in metadata. The recommended practice is that vernacular names be used
                consistently within a dataset.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="scientificName" ref="dwc:scientificName" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The taxonomic identification of the observation as either 1) Genus
                and species (and subspecies if provided) in Latin binomial nomenclature form, or 2)
                the lowest-level taxonomic name to which the observation is identified, expressed in
                Latin form. scientificName is a required term. Authorities, references and
                procedures for making identifications should be documented in
                metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="taxonRank" ref="dwc:taxonRank" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The taxonRank term is a companion to the scientificName term.
                taxonRank identifies the taxonomic level of the lowest-level name in the
                scientificName term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="aphiaID" ref="ioosbiology:aphiaID" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A unique taxon identifier obtained by validation of the taxon name
                with the World Register of Marine Species (WoRMS),
                www.marinespecies.org.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="tsn" ref="ioosbiology:tsn" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A unique taxon identifier obtained by validation of the taxon name
                with the Integrated Taxonomic Information System (ITIS),
                www.itis.gov.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!--  Occurrence detail terms  -->

    <xsd:element name="individualCount" ref="dwc:individualCount" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The number of individuals represented in the observation record.
                Valid values include positive integers, zero, and null. Positive integers represent
                presence. If the observation record and metadata also contain other required
                information such as details about the sampling activity, individualCount can
                contribute to the abundance calculations. Null value for individualCount represents
                a record of presence, with quantity unspecified, and null values do not support
                abundance calculations. Zero value represents absence. Zero values for absence are
                only valid if methodology for establishing absence is recorded in
                metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sex" ref="dwc:sex" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The sex of biological individuals represented in the observation
                record. Vocabulary will be consistent within a dataset and will be explained in
                metadata. Methods of determination (where applicable) will be explained in
                metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="lifeStage" ref="dwc:lifeStage" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>An expression or description of age or lifestage of biological
                individual(s) in the observation record. Vocabulary will be consistent within a
                dataset and will be explained in metadata. Methods of determination (where
                applicable) will be explained in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observedIndividualLengthInCm" ref="ioosbiology:observedIndividualLengthInCm"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>If a single individual is observed and measured, record length in
                centimeters here.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observedMeanLengthInCm" ref="ioosbiology:observedMeanLengthInCm"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>If measuring more than one individual for aggregate length values,
                record mean length in centimeters here.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observedMaxLengthInCm" ref="ioosbiology:observedMaxLengthInCm"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>If measuring more than one individual for aggregate length values,
                record maximum length in centimeters here.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="observedMinLengthInCm" ref="ioosbiology:observedMinLengthInCm"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>If measuring more than one individual for aggregate length values,
                record minimum length in centimeters here.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="lengthType" ref="ioosbiology:lengthType" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The type or method of length measurement used in this observation
                record, such as TL for total length, FL for fork length, SL for standard
                length.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!-- Sample identification and sampling event terms  -->

    <xsd:element name="sampleID" ref="ioosbiology:sampleID" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A unique identifier for a unit of material that serves as a sample
                for a survey of biological occurrence (presence, absence or derived value). The
                definition of a sample and assignment of IDs is cojntroled by the data originator.
                If applicable, details about how sample ares are defined and IDs assigned will be
                provided in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="subsampleID" ref="ioosbiology:subsampleID" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>If a sample is further divided by the data originator for purposes of
                organization, handling or analysis, and if the data originator wants to maintain the
                identity of the subsample, capture the ID of the subsample here. Explain in metadata
                if applicable.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="samplingProtocol" ref="dwc:samplingProtocol" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Information about the sampling method as defined by the data
                originator. Valid values include S for stationary, T for towed, D for diver swim.
                Contents or vacabulary used in this term will be used consistently in a dataset and
                will be explained in metadata. Additional information can be concatenated into the
                term, delimited by semicolon. More extensive discussion of sampling protocol, effort
                and conditions may be provided in metadata as needed.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="samplingEffort" ref="dwc:samplingEffort" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Information about the extent, duration or other variable aspects of
                the sampling activity, as conducted by the data originator, that occurred at the
                time of the sampling event. More than one type of effort information can be
                concatenated into this term, delimited by semicolon. Other terms are available in
                this terminology for some specific details of sampling effort, such as sample
                dimensions, that are expected to be frequently used in IOOS services. Use the
                samplingEffort term for additional effort information that is not addressed by other
                terms. More extensive discussion of sampling protocol, effort and conditions may be
                provided in metadata as needed.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="samplingConditions" ref="ioosbiology:samplingConditions" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Information about the state of the sampling location, determined by
                external factors such as weather, at the time of the sampling event. More than one
                type of information about conditions can be concatenated into this term, delimited
                by semicolon. Other terms are available in this terminology for some specific
                details of sampling conditions, such as habitat, bottomType, visibilty and
                temperature, that are expected to be frequently used in IOOS services. Use the
                samplingConditions term for additional information about conditions that is not
                addressed by other terms. More extensive discussion of sampling protocol, effort and
                conditions may be provided in metadata as needed.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleShape" ref="ioosbiology:sampleShape" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The shape of the sample space in which the observation was made, such
                as R for rectangular, C for cylindrical.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleWidthInMeters" ref="ioosbiology:sampleWidthInMeters" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The width in meters of the sample space in which the observation was
                made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleHeightInMeters" ref="ioosbiology:sampleHeightInMeters"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The length in meters of the sample space in which the observation was
                made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleRadiusInMeters" ref="ioosbiology:sampleRadiusInMeters"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The radius in meters of a cylindrical sample
                space.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleAreaInSquareMeters" ref="ioosbiology:sampleAreaInSquareMeters"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The area in square meters, if projected vertically to a plane
                representing the ocean surface, of the sample space in which the observation was
                made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="sampleVolumeInCubicMeters" ref="ioosbiology:sampleVolumeInCubicMeters"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The volume in cubic meters of the sample space in which the
                observation was made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="visibilityInMeters" ref="ioosbiology:visibilityInMeters" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Visibility through the water column in meters.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="visibilityType" ref="ioosbiology:visibilityType" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The direction of estimated visibility, horizontal or
                vertical.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="waterTemperatureInCelsius" ref="ioosbiology:waterTemperatureInCelsius"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The temperature of the water at the time of the observation,
                expressed in degrees Celsius.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="habitat" ref="dwc:habitat" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A description or identifier of general information about the habitat
                in which the observation was made. Vocabulary will be consistent within a dataset
                and will be explained in metadata. Methods of determination (where applicable) will
                be explained in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="bottomType" ref="ioosbiology:bottomType" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A description or identifier of general information about the sea
                floor at the coordinates or locality where the observation was made. Vocabulary will
                be consistent within a dataset and will be explained in metadata. Methods of
                determination (where applicable) will be explained in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!-- Quantification terms  -->

    <xsd:element name="quantificationVocabulary" ref="ioosbiology:quantificationVocabulary"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The names for dervied values, referred to as "quantification", can be
                drawn from a controlled vocabulary or vocabularies of quantification names. Or they
                can be reported in IOOS services using the verbatim name given by the data
                originator. Either the name of a controlled vocabulary or the word "verbatim" should
                be used in this term. Either way, within a dataset, both verbatim and vocabulary
                names must be used consistently, and explained in metadata.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationName" ref="dwc:measurementType" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A name for a derived value or processed data about the occurrence,
                for example, "Biomass". The word used in this terminology for such information is
                "quantification", rather than "abundance", because "abundance" may have specific
                methodological immplications in biology. In this example, biomass would not be
                obtained at survey time, rather biomass would be calculated from input data that was
                obtained at survey time, combined with a biomass calculation methodology. This term
                is used along with companion terms for quantification value, units, uncertainty,
                method, and determination details. It is suggested that names for derived values be
                more specific than "Biomass", because many institutions will develop biomass
                information using diverse methods. Suggested practice is to include some more
                specific reference(s) in the quantification name, such as insitution, survey, date
                or other specifics. For example, "Biomass-PIFSC-2011", and explain naming in
                metadata. </xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationValue" ref="dwc:measurementValue" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The value of the derived information product, such as the numerical
                value for biomass. This term does not include units. Units are contained in another
                term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationUnit" ref="dwc:measurementUnit" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The units in which the value expresses the quantification, for
                example, "kg/m^2 surface" or "kilograms per square meter of ocean
                surface".</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationUncertainty" ref="dwc:measurementAccuracy" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>An estimate of the uncertainty, positive or negative (+/-) offset of
                the stated value, that expresses the uncertainty of the value as calculated and
                reported. Note that the expression in this term can combine both accuracy and
                precision considerations to a more general estimate, uncertainty, hence the slightly
                different name for this term from compared to the Darwin Core (dwc) reference
                term.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationDeterminedDate" ref="dwc:measurementDeterminedDate"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The date the quantification was determined. Can be different from the
                observation date.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationDeterminedBy" ref="dwc:measurementDeterminedBy"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name or ID of person(s) or institution(s) that determined the
                quantification.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="quantificationMethod" ref="dwc:measurementMethod" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A reference to the method used to determine the quantification. This
                will be different from the method used to make the observation of biological
                occurrence; it will be the companion calucation method that followed the observation
                method. Quantification information is expected to be only useful if method is
                sufficiently documented, so this term is vitally important for use of quantification
                terms for derived values. This term can contain a code or other abbreviated
                reference to a method. In all cases quantificationMethod should be explained in
                metadata and supporting publications or related resources
                identified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <!-- Named geography terms  -->

    <xsd:element name="waterBody" ref="dwc:waterBody" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of the water body in which the observation was made. For
                marine data, this is the ocean name. If there is a more specific named region, such
                as a bay or reef, or sector of the ocean (for example, northwest Pacific), add the
                regional name after the ocean name, separated by a semicolon. Note that the locality
                term will contain the most specific name, such as a pier or other named feature, so
                that lowest level of detail is not included in waterbody. The waterbody term is for
                the ocean and any named intermediate geography such as a region.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="islandGroup" ref="dwc:islandGroup" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of an island group associated with the location where the
                observation was made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="island" ref="dwc:island" type="xsd:">
        <xsd:annotation>
            <xsd:documentation>The name an island associated with the location where the observation
                was made.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="locality" ref="dwc:locality" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The locality is the most specific named place to identify the
                location of the observation. Many marine data rely strictly on geographic
                coordinates, so the locality term may be null. If a locality is used, it may be a
                specific location or feature name, such as "Pier 39" or "Atafu Atoll", or it may be
                a descriptive phrase, such as "a tidal pool 1500 meters north of Pier 39". Note that
                in marine observations, the latitude and longitude may be more precise than any
                named place would suggest, because the coordinates often come from navigation of GPS
                systems. Place names can be secondary locality identifiers and thus less precise
                than coordinates.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="country" ref="dwc:country" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of the country in which the observation location
                ocurs.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="stateProvince" ref="dwc:stateProvince" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of the state or province in which the observation location
                ocurs. Such geographic named locations may not be available or applicable for marine
                data, and acordingly the use of this term is optional. In some cases such
                jurisdiction identification may be crucial for data attribution, management and/or
                use, so this term is retained in the terminology for cases where it may be
                essential.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="county" ref="dwc:county" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of the county or other comparable geographic unit in which
                the observation location ocurs. Such geographic named locations may not be available
                or applicable for marine data, and acordingly the use of this term is optional. In
                some cases such jurisdiction identification may be crucial for data attribution,
                management and/or use, so this term is retained in the terminology for cases where
                it may be essential.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="municipality" ref="dwc:municipality" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name of the municipality in which the observation location ocurs.
                Such geographic named locations may not be available or applicable for marine data,
                and acordingly the use of this term is optional. In some cases such jurisdiction
                identification may be crucial for data attribution, management and/or use, so this
                term is retained in the terminology for cases where it may be
                essential.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="geodeticDatum" ref="dwc:geodeticDatum" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The ellipsoid, geodetic datum, or spatial reference system used in
                decimalLatitude and decimalLongitude. IOOS preference is to provide all coordinates
                using EPSG:4326, also known as WGS 84. This element will identify the actual datum
                used, confirming WGS 84 or identifying what other datum applies.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="kingdom" ref="dwc:kingdom" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the kingdom in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="phylum" ref="dwc:phylum" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the phylum in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="class" ref="dwc:class" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the class in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="order" ref="dwc:order" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the order in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="family" ref="dwc:family" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the family in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="genus" ref="dwc:genus" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the genus in which the taxon is
                classified.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="subgenus" ref="dwc:subgenus" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the subgenus in which the taxon is
                classified. Values should include the genus to avoid homonym
                confusion.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="species" ref="dwc:specificEpithet" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the species in which the taxon is
                classified. If a subspecies identification is provided, add the subspecies name
                after the species name separated by a space.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="infraspecificEpithet" ref="dwc:infraspecificEpithet" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The full scientific name of the subspecies, variant or other finer
                level identification.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="scientificNameAuthorship" ref="dwc:scientificNameAuthorship"
        type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The authorship information for the
                scientificName.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="taxonRemarks" ref="dwc:taxonRemarks" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Comments or notes about the taxon or name.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="identifiedBy" ref="dwc:identifiedBy" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The name or other identifier of individual(s) or institution(s) that
                assigned the taxonomic name. Can be a list delimited by
                semicolon.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="identificationDate" ref="dwc:eventDate" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>The date the identification on this record was made, expressed in ISO
                8601 date format.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="identificationQualifier" ref="dwc:identificationQualifier" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>A brief phrase or a standard term ("cf.", "aff.") to express the
                determiner's doubts about the Identification.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

    <xsd:element name="identificationRemarks" ref="dwc:identificationRemarks" type="xsd:string">
        <xsd:annotation>
            <xsd:documentation>Comments or notes about the identification.</xsd:documentation>
        </xsd:annotation>
    </xsd:element>

</xsd:schema>

```

## Version 0.9

* Originally submitted by Philip Goldstein, USGS/OBIS-USA on 2011-11-30
* [IOOS Biological Data Terminology version 0.9: Definition](http://www.ioos.noaa.gov/schema/ioosbiology/0_9/ioos_biological_terminology_vpoint9d.xml)
* [IOOS Biological Data Terminology version 0.9 (xsd)](http://www.ioos.noaa.gov/schema/ioosbiology/0_9/ioosbiologicalterminology_vpoint9.xsd)



