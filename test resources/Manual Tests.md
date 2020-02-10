Notes on verifing HAPI FHIR and measures.
==========================================

Original Data Source: DBCG/connectathon (https://github.com/DBCG/connectathon.git)

Data sample fetched in late October 2019

The code server is: https://matdev.semanticbits.com/hapi-fhir-jpaserver/fhir and the certificate is self-signed. If using postman, the setting item should have validate ssl certificate disabled.
 
The entire test set is the Postman collection FHIR R4 Measures.postman_collection.json

Note that returned data is currently manually pretty printied at https://jsonformatter.org before being compared with the original source. 

#Future work:   

    * Now that the sample completeness is known update the base sample to have the sample field order as returned by HAPI or use a json level comparison tool.
    * Update the postman to include automated formatting and comparison.
    
#Additional notes:

	  * 100% comparison on the server us not possible due to the version metadata being updated. This and field order are the only known differences.
	  * After a reflexive conversion of JSON top XML, the XML to JSON the field Measue.text._status.fhircomments is added - Contents appear to be junk.  
    