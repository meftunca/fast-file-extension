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
  -  `\BT` `BT/` or `\BF` `BF/`
- NULL IS : `\N` `N/` or null
- ...


### Warning information for everybody

Parsing is based entirely on token generation adhering to regular expressions. Fast data processing will be possible thanks to certain rules. The project is currently experimental. Please do not use the sample codes in your projects that you will publish.
