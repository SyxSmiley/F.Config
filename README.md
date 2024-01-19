# F.Config


F.Config is a simple gui based application to set comments and variables at a Fanuc Robot over HTTP requests.

![image](https://github.com/SyxSmiley/F.Config/assets/101479924/d39835e1-7644-40f2-a1e4-8205c3ae16c0)


## Supportet modes

1. Transfer configuration file
2. Load configuration and save it in a configuration file
3. Direct input for a single value


## Transfer configuration file
The configuration file has to be an .ini file

A new configuration area start with a configuration key in brackets [key]

### Possible keys

Robot input [ RDI | RI ]  

Robot output [ RDO | RO ]

Digital input [ DIN | DI ]

Digital output [ DOUT | DO ] 

Group output [ GOUT | GO ] 

Group input  [ GIN | GI ] 

Analog output [ AOUT | AO ] 

Analog input  [ AIN | AI ] 

Flag [ FLG | F ]

Variable [ VAR ]

The configuration key is followed by all associated configurations starting with the index / variable name assigned by the comment/value

e.g. 1=Test comment
