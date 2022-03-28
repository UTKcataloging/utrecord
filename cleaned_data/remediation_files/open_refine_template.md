# Open Refine Template University of Tennessee Record


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 

<titleInfo supplied="yes"><title>{{cells['title_supplied'].value}}</title></titleInfo>

<titleInfo type="alternative"><title>{{cells['title_alternative'].value}}</title></titleInfo>

{{if(isBlank(cells['dateIssued'].value), '', '<originInfo><dateIssued>' + cells['dateIssued'].value + '</dateIssued><dateIssued encoding="edtf">' + cells['dateissued_EDTF'].value + '</dateIssued>' + if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher><place><placeTerm valueURI="http://id.loc.gov/authorities/names/n79109786">Knoxville (Tenn.)</placeTerm>
</place>') + '</originInfo>')}}

<abstract>{{cells["abstract"].value}}</abstract>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["extent"].value}}</extent></physicalDescription>

{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}

{{if(isBlank(cells['frequencyInfo'].value), '', '<note>' + cells['frequencyInfo'].value + '</note>')}}

{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject5'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject5_URI'].value + '"><topic>' + cells['subject5'].value + '</topic></subject>')}}


{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_2_URI'].value + '"><name><namePart>' + cells['subject_name_2'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_3'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_3_URI'].value + '"><name><namePart>' + cells['subject_name_3'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_4'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_4_URI'].value + '"><name><namePart>' + cells['subject_name_4'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_5'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_5_URI'].value + '"><name><namePart>' + cells['subject_name_5'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_name_6'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_6_URI'].value + '"><name><namePart>' + cells['subject_name_6'].value + '</namePart></name></subject>')}}

<subject authority="naf" valueURI="{{cells['subject_geography_URI'].value}}"><geographic>{{cells['subject_geographic'].value}}</geographic></subject>

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
{{if(isBlank(cells['typeOfResource2'].value), '', '<typeOfResource>' + cells['typeOfResource2'].value + '</typeOfResource>')}}

<classification authority="lcc">{{cells['classification'].value}}</classification>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>University of Tennessee Record</title></titleInfo></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```