!SLIDE

# JSON #
## JavaScript Object Notation ##

!SLIDE smbullets small
# Wha? #
* JSON is a (relatively) lightweight format for pushing around data.
* Not language dependent (you don't have to be using JavaScript)
* It is extremely simple (it pretty much just uses two structures)
* You don't need XPath to find stuff

!SLIDE small smbullets
# There can be only <strike>one</strike> two
* Objects: A set of key/value pairs.  Think "dictionary" or "hash table"
* Objects look like   { "Key1" : "Value1", "Key2" : "Value2" }
* Arrays: An ordered set of values.  Think "array"
* Arrays look like [ "Value1", "Value2" ]
* Values can be additional objects or arrays

!SLIDE small
# JSON and XML examples #

!SLIDE code smaller
    @@@javascript
    borrowed from json.org
    {
        "glossary": {
            "title": "example glossary",
            "GlossDiv": {
                "title": "S",
                "GlossList": {
                    "GlossEntry": {
                        "ID": "SGML",
                        "SortAs": "SGML",
                        "GlossTerm": "Standard Generalized Markup Language",
                        "Acronym": "SGML",
                        "Abbrev": "ISO 8879:1986",
                        "GlossDef": {
                            "para": "A meta-markup language, used to create markup languages such as DocBook.",
                            "GlossSeeAlso": ["GML", "XML"]
                        },
                        "GlossSee": "markup"
                    }
                }
            }
        }
    }

!SLIDE code smaller
    @@@xml
    still borrowed from json.org
    <!DOCTYPE glossary PUBLIC "-//OASIS//DTD DocBook V3.1//EN">
     <glossary><title>example glossary</title>
      <GlossDiv><title>S</title>
       <GlossList>
        <GlossEntry ID="SGML" SortAs="SGML">
         <GlossTerm>Standard Generalized Markup Language</GlossTerm>
         <Acronym>SGML</Acronym>
         <Abbrev>ISO 8879:1986</Abbrev>
         <GlossDef>
          <para>A meta-markup language, used to create markup
    languages such as DocBook.</para>
          <GlossSeeAlso OtherTerm="GML">
          <GlossSeeAlso OtherTerm="XML">
         </GlossDef>
         <GlossSee OtherTerm="markup">
        </GlossEntry>
       </GlossList>
      </GlossDiv>
     </glossary>

!SLIDE small smbullets
# So Why Does This Matter? #
* JSON is really just an array.
* Load it into a language that gets it (like JavaScript) and it's now an in memory object
* No XPath!

!SLIDE smaller code
    @@@javascript
    var object = SomeMethodThatReturnsJson();

    var value = object.glossary.GlossDiv[2].ID;     

!SLIDE small smbullets
# Sending JSON Client-Side #
* Most languages can read/write JSON 
* In ASP.NET MVC there is a JsonResult ViewResult.  You just "return Json(yourObject);"
* WCF can be configured to use JSON instead of XML (example [here](http://dotnetslackers.com/articles/ajax/JSON-EnabledWCFServicesInASPNET35.aspx))

!SLIDE
# Questions? #
