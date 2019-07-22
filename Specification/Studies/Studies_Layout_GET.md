## Plot Layout Details [/brapi/v1/studies/{studyDbId}/layout]
Scope: PHENOTYPING.

### Retrieve plot layout details [GET /brapi/v1/studies/{studyDbId}/layout{?pageSize}{?page}]

Retrieve the plot layout of the study with id {id}.

For each observationUnit within a study, return the `block`, `replicate`, and `entryType` values as well as the `X` and `Y` coordinates. `entryType` can be "check", "test", or "filler".

Also return some human readable meta data about the observationUnit and germplasm.

+ Parameters
    + studyDbId (required, string, `1`) ... Identifier of the study.
    + pageSize (optional, integer, `1000`) ... The size of the pages to be returned. Default is `1000`.
    + page (optional, integer, `0`) ... Which result page is requested. The page indexing starts at 0 (the first page is 'page'= 0). Default is `0`.

+ Response 200 (application/json)
    
        {
            "metadata" : {
                "pagination": {
                    "pageSize": 1000,
                    "currentPage": 0,
                    "totalCount": 4,
                    "totalPages": 1
                },
                "status": [],
                "datafiles": []
            },
            "result" : {
                "data" : [ 
                    {
                        "studyDbId": "1",
                        "observationUnitDbId": "11",
                        "observationUnitName": "ZIPA_68_Ibadan_2014",
                        "observationLevel": "plot",
                        "germplasmDbId": "143",
                        "germplasmName": "ZIPA_68",
                        "replicate": 1,
                        "blockNumber": 1,
                        "X": 1,
                        "Y": 1,
                        "entryType": "check/test/filler",
                        "additionalInfo" : { 
                        }
                    },
                    {
                        "studyDbId": "1",
                        "observationUnitDbId": "12",
                        "observationUnitName": "ZIPA_69_Ibadan_2014",
                        "observationLevel": "plot",
                        "germplasmDbId": "144",
                        "germplasmName": "ZIPA_69",
                        "replicate": 1,
                        "blockNumber": 1,
                        "X": 1,
                        "Y": 2,
                        "entryType": "check/test/filler",
                        "additionalInfo" : { 
                        }
                    },
                    {
                        "studyDbId": "1",
                        "observationUnitDbId": "13",
                        "observationUnitName": "ZIPA_70_Ibadan_2014",
                        "observationLevel": "plot",
                        "germplasmDbId": "145",
                        "germplasmName": "ZIPA_70",
                        "replicate": 1,
                        "blockNumber": 1,
                        "X": 1,
                        "Y": 3,
                        "entryType": "check/test/filler",
                        "additionalInfo" : { 
                        }
                    },
                    {
                        "studyDbId": "1",
                        "observationUnitDbId": "11",
                        "observationUnitName": "ZIPA_68_Ibadan_2014",
                        "observationLevel": "plot",
                        "germplasmDbId": "143",
                        "germplasmName": "ZIPA_68",
                        "replicate": 2,
                        "blockNumber": 2,
                        "X": 2,
                        "Y": 1,
                        "entryType": "check/test/filler",
                        "additionalInfo" : { 
                        }
                    }
                ]
            }
        }
