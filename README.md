![](https://dev.lutece.paris.fr/jenkins/buildStatus/icon?job=tech-plugin-geocodesclient-deploy)
[![Alerte](https://dev.lutece.paris.fr/sonar/api/project_badges/measure?project=fr.paris.lutece.plugins%3Aplugin-geocodesclient&metric=alert_status)](https://dev.lutece.paris.fr/sonar/dashboard?id=fr.paris.lutece.plugins%3Aplugin-geocodesclient)
[![Line of code](https://dev.lutece.paris.fr/sonar/api/project_badges/measure?project=fr.paris.lutece.plugins%3Aplugin-geocodesclient&metric=ncloc)](https://dev.lutece.paris.fr/sonar/dashboard?id=fr.paris.lutece.plugins%3Aplugin-geocodesclient)
[![Coverage](https://dev.lutece.paris.fr/sonar/api/project_badges/measure?project=fr.paris.lutece.plugins%3Aplugin-geocodesclient&metric=coverage)](https://dev.lutece.paris.fr/sonar/dashboard?id=fr.paris.lutece.plugins%3Aplugin-geocodesclient)

# Plugin geocodes client

## Introduction

The purpose of this plug-in is to provide a local REST service to call geocodes services.

## Configuration



## Usage

Use the lutece @autocomplete macro, with the local suggestion URLs :

 
* GET /rest/geocodesclient/api/v1/cities
* GET /rest/geocodesclient/api/v1/countries

Example :

 
* <@input type='date' id='birthdate' name='birthdate' />
* <@input type='text' id='birthplace_code' name='birthplace_code' />
* <@input type='text' id='birthplace' name='birthplace' />
* <@autocomplete id="autocompleteBirthPlace" name="" itemValueFieldName="displayValue" suggestionsUrl="rest/geocodesclient/api/v1/cities?search=" suggestionsPath="result" itemTitleFieldNames='["value","codeZone"]' minimumInputLength=3 additionnalRequestParamInputId="birthdate" copyFields='[{"inputName":"birthplace_code","resultFieldName":"code"},{"inputName":"birthplace","resultFieldName":"value"}]' />
* <@input type='text' id='birthcountry_code' name='birthcountry_code' />
* <@input type='text' id='birthcountry' name='birthcountry' />
* <@autocomplete id="autocompleteBirthCoutnry" name="" itemValueFieldName="value" suggestionsUrl="rest/geocodesclient/api/v1/countries?search=" suggestionsPath="result" itemTitleFieldNames='["value"]' minimumInputLength=3 additionnalRequestParamInputId="birthdate" copyFields='[{"inputName":"birthcountry_code","resultFieldName":"code"},{"inputName":"birthcountry","resultFieldName":"value"}]' />


[Maven documentation and reports](https://dev.lutece.paris.fr/plugins/plugin-geocodesclient/)



 *generated by [xdoc2md](https://github.com/lutece-platform/tools-maven-xdoc2md-plugin) - do not edit directly.*