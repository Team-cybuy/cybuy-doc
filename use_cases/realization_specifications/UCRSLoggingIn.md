# 1.	Introduction

## 1.1	Purpose
This Use-Case Realization Specification (UCRS) describes all specifications for the Use-Case “Logging in” for the webservice “cybuy”. It includes an overview and more detailed information about the planned implementation of the use case.

## 1.2	Scope
Access to our webservice will be provided through a web interface on a website.
No standalone apps are planned.
This Use-Case applies to the Account System:
Persistent accounts can be created, managed and deleted with the associated credentials.
User data is stored server side and if possible in hashed or encrypted form.
Exceptions may be made for image contents with third party hosting providers.

## 1.3	Definitions, Acronyms, and Abbreviations
| Abbrevation | Explanation                            |
| ----------- | -------------------------------------- |
| UCRS        | Use-Case Realization Specification     |
| n/a         | not applicable                         |
| tbd         | to be determined                       |


## 1.4	References
| Title                                                  | Organisation |
| ------------------------------------------------------ | ------------ |
| [Code Repository](https://github.com/Team-cybuy/cybuy) | Team cybuy   |
| [Blog](https://medium.com/@cybuysite)                  | Team cybuy   |

## 2.	Flow of Events—Design 
![Flow of Events](/resources/sequence_diagrams/SequenceDiagramLogginIn.png)