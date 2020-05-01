# Menota Snippets

This Extension contains a set of snippets to increase productivity when transcribing medieval nordic manuscripts in Menota TEI XML.

For more information on Menota, see [menota.org](https://menota.org/forside.xhtml) or the [Menota handbook](https://menota.org/HB3_index.xml).

## How To Use

When in an XML file, hit `Ctrl + Space` to open intellisense code completion, or simply start typing `me:`.  
VS Code will suggest the Menota snippets, pick the one you want with the arrow keys (or by continuing to type) ant then hint `Enter`.

The caret will automatically be at the fist place you need to fill in. Keep filling in and hitting `Tab` to jump to the next section.


## Features

### Overview

Adds the following snippets:

- `me:document`: template document to start transcribing from. (Including minimal header and document structure. Insert it at the beginning, then modify afterwards.)
- `me:word`: Word tag in three level transcription.

### Details

#### Document
`me:document` is resolved into:
```XML
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE TEI 
[
<!ENTITY % Menota_entities SYSTEM 'http://www.menota.org/menota-entities.txt'>
%Menota_entities; ]>

<TEI  xmlns="http://www.tei-c.org/ns/1.0"
    xmlns:me="http://www.menota.org/ns/1.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://www.tei-c.org/ns/1.0 https://raw.githubusercontent.com/BalduinLandolt/menota-xsd-schema/master/menota.xsd">
    <teiHeader>
        <fileDesc>
            <titleStmt>
                <title>title</title>
                <editor>your_name</editor>
            </titleStmt>
            <editionStmt>
                <p></p>
            </editionStmt>
            <extent></extent>
            <publicationStmt>
                <p></p>
            </publicationStmt>
            <notesStmt>
                <note></note>
            </notesStmt>
            <sourceDesc>
                <msDesc>
                    <msIdentifier>
                        <idno>shelfmark</idno>
                    </msIdentifier>
                </msDesc>
            </sourceDesc>
        </fileDesc>
    </teiHeader>
    <text>
        <body>
            <div>
                <p>
                    <!-- Start Transcribing here -->
                    
                    
                    
                    
                </p>
            </div>
        </body>
    </text>
</TEI>
```

Note: Only the most important fields of the header ("title", "editor" and "idno") are marked with placeholders (hit `Tab` to traverse them).  
Be sure to add all necessary information to the header in due time. An extensive guide can be found [here](https://www.menota.org/HB3_ch14.xml).

#### Word
`me:word` is resolved into:
```XML
<w>
    <me:facs>facs</me:facs>
    <me:dipl>dipl</me:dipl>
    <me:norm>norm</me:norm>
</w>
```

## Requirements

None.

## Extension Settings

Contributes: the above named snippets.

## Known Issues

None.

## Feedback and Contributions.

Any feedback is most welcome. If you have any suggestions or wishes, or if there are more snippets you feel should be added, please create an [Issue on Github](https://github.com/BalduinLandolt/vscode-menota-snippets/issues).

## Release Notes

### 1.0.0

Initial release.
