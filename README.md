# F.Config V0.1


F.Config is a simple gui based application to set comments and variables at a Fanuc Robot over HTTP requests.

![image](https://github.com/SyxSmiley/F.Config/assets/101479924/d39835e1-7644-40f2-a1e4-8205c3ae16c0)


# Supportet modes

1. Transfer configuration file
2. Load configuration and save it in a configuration file
3. Direct input for a single value


# Transfer configuration file
The configuration file has to be an .ini file

A new configuration area start with a configuration key in brackets [key]

## Possible keys

Robot input [ RDI | RI ]  

Robot output [ RDO | RO ]

Digital input [ DIN | DI ]

Digital output [ DOUT | DO ] 

Group output [ GOUT | GO ] 

Group input  [ GIN | GI ] 

Analog output [ AOUT | AO ] 

Analog input  [ AIN | AI ] 

Flag [ FLG | F ]

Numeric register [ NUMREG | R ]

Position register [ POSREG | PR ]

String register [ STRREG | SR ]

User alarms [ UALARM | UALM ]

Variable [ VAR ]


## Assignment
The configuration key is followed by all associated configurations starting with the index/variable name assigned by the comment/value e.g. 

[DI]

1=Test comment

[VAR]

$KAREL_ENB=1

## Range
To assign multiple equal or similar comments it is possible to define a range before the assignment e.g.

[DI]

1-10=Test comment

### Placeholder 
If the comment has a increasing number it is possible to combine a range assignment with **one** placeholder. 

The placeholder is definded by a $ and it is replaced with 0 or the value after the $. For each comment in the range the placeholder is increased by 1. e.g.

[DI]

1-10=Test comment $ 

11-20=Test comment $5 

# Load configuration file
Load the actual configuration of the robot and save into a configuration file. The file will be saved in the download folder.

## Limitation
Only connected IOs are saved into the configuration file 

# Direct input
Direct input allows you to set a comment or variable directly without using a configuration file

# Language
Supportet languages are
1. Englisch
2. German















