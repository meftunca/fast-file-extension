# Fast File (.ff)

## Data format and syntax for projects that need to write/read large amounts of data.

### RULES

### Spesific Escape String Literals

- Object IS : `\O O/` or `\{ }/`
- Array IS : `\A A/` or `\[ ]/`
- String IS : `\(` `)/`
- Number IS : `\N` `N/`
- Object Key IS : `\OK` `OK/`
- BOOLEAN IS : true or false 
  -  `\T/` or `\F/`
- NULL IS : `\NA/` or null
- ...


### Warning information for everybody

Parsing relies entirely on token generation or any search algorithm, adhering to regular expressions. Fast data processing will be possible thanks to certain rules. The project is currently experimental. Please do not use sample codes in your projects that you will publish.

May require 4% ~ 6% more data size than JSON files.


### Examples

```
\O
  /OKexamplesOK/: /A
    \O
      /OKtag_nameOK/: /(a)/,
      /OKattrOK/: /A
        \O
          /OKkeyOK/: /(href)/,
          /OKvalueOK/: /(http://amir.saboury.net)/
        O/,
       \O
          /OKkeyOK/: /(target)/,
          /OKvalueOK/: /(_blank)/
        O/
      A/
    O/,
   \O
      /OKthis_isOK/: /A
        /(array)/,
        /(of)/,
        /(strings)/
      A/,
      /OKnumber_arrayOK/: /A
        \N1N/,
        \N2N/,
        \N4N/,
        \N8N/,
        \N16N/
      A/,
      /OKpieOK/: \N3.14N/,
      /OKbooleanOK/: \T/,
      /OKbugOK/: \NA/,
      /OKmixedOK/: /A
        \N1N/,
        \N2N/,
        /O
          /OKtest1OK/: -1.2345,
          /OKtest2OK/: \F/
        O/,
        \NA/,
        \N0.4N/,
        /A
          /(nested)/,
          /A
            /(array)/,
            \T/
          A/
        A/,
        /(end of story!)/
      A/
    O/,
    \O
      /OKdoneOK/: \T/
   O/
  A/
O/

```
