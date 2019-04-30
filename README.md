    <link href="yasgui.bootstrap.css" rel="stylesheet" type="text/css">
    <link href="yasgui.min.css" rel="stylesheet" type="text/css">
    <script src="yasgui.min.js"></script>
    <script src="yasgui.polyfill.min.js"></script>
    <script type="text/javascript">
    window.onload = function () {
    Yasgui.stories()
    };
    </script>
    
    <query data-config="http://127.0.0.1:5000/stories/OpenELS/#query=PREFIX+rdf%3A+%3Chttp%3A%2F%2Fwww.w3.org%2F1999%2F02%2F22-rdf-syntax-ns%23%3E%0APREFIX+rdfs%3A+%3Chttp%3A%2F%2Fwww.w3.org%2F2000%2F01%2Frdf-schema%23%3E%0APrefix+au%3A+%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23%3E%0ASELECT+%3Fcountry+(group_concat(distinct+%3F1stName%3Bseparator%3D'%2C')+as+%3F1stLevel)+(group_concat(distinct+%3F2ndName%3Bseparator%3D'%2C')+as+%3F2ndLevel)++(group_concat(distinct+%3F3rdName%3Bseparator%3D'%2C')+as+%3F3rdLevel)%0AWHERE+%7B%0A%7B++Values+(%3Fg+%3Fcountry)+%7B(%3Chttp%3A%2F%2Fdata.labs.pdok.nl%2Fdataset%2Fopenels%2Fau%3E+%22The+Netherlands%22)%7D%0A++graph+%3Fg+%7B%0A++++++%3Fau1st+au%3AAdministrativeUnit.nationalLevel+%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Fcodelist%2FAdministrativeHierarchyLevel%2F1stOrder%3E%3B%0A+++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F1stName.%0A+++++++%3Fau2nd+au%3AAdministrativeUnit.nationalLevel+%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Fcodelist%2FAdministrativeHierarchyLevel%2F2ndOrder%3E%3B%0A+++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F2ndName.%0A+++++++%3Fau3rd+au%3AAdministrativeUnit.nationalLevel+%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Fcodelist%2FAdministrativeHierarchyLevel%2F3rdOrder%3E%3B%0A+++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F3rdName.%0A+++++%7D%0A%7D%0A++Union%0A++++%7B%0A++SERVICE+%3Chttp%3A%2F%2Frdf.kartverket.no%2F%2Fsparql%3E+%7B%0A++++++Values+(%3Fg+%3Fcountry)+%7B(%3Chttp%3A%2F%2Fopenels%2Fadministrativeunits%3E+%22Norway%22)%7D%0A++graph+%3Fg+%7B%0A++++%3Fau2nd+au%3AAdministrativeUnit.nationalLevel+%222ndOrder%22%3B%0A++++++++++++++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F2ndName.%0A++++%3Fau1st+au%3AAdministrativeUnit.nationalLevel+%221stOrder%22%3B%0A++++++++++++++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F1stName.%0A++++%3Fau3rd+au%3AAdministrativeUnit.nationalLevel+%223rdOrder%22%3B%0A++++++++++++++++++++++++%3Chttp%3A%2F%2Finspire.ec.europa.eu%2Font%2Fau%23AdministrativeUnit.nationalLevelName%3E+%3F3rdName.%0A++%7D%0A++++%7D%0A++%7D%0A%7D%0AGroup+by+%3Fcountry%0A%0A&contentTypeConstruct=text%2Fturtle&contentTypeSelect=application%2Fsparql-results%2Bjson&endpoint=https%3A%2F%2Fdata.labs.pdok.nl%2Fopenels%2Fsparql&requestMethod=POST&tabTitle=Query&headers=%7B%7D&outputFormat=table"
           data-endpoint="https://data.labs.pdok.nl/openels/sparql"
           data-query-ref="levels_names.rq"
           data-output="table">
    </query>

# SemInt2019
rep for test
