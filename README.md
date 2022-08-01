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
- NULL IS : `\N/` or null
- ...


### Warning information for everybody

Parsing is based entirely on token generation adhering to regular expressions. Fast data processing will be possible thanks to certain rules. The project is currently experimental. Please do not use the sample codes in your projects that you will publish.


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
        1,
        2,
        4,
        8,
        16
      A/,
      /OKpieOK/: 3.14,
      /OKbooleanOK/: \T/,
      /OKbugOK/: \N/,
      /OKmixedOK/: /A
        1,
        2,
        /O
          /OKtest1OK/: -1.2345,
          /OKtest2OK/: \F/
        O/,
        \N/,
        0.4,
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
