## 📌 Description
evaluate code interpolating vtk array names as symbols
creates new arrays or update existing ones
## 📸 Screenshot
![screenshot1](https://github.com/pemn/assets/blob/main/vtk_evaluate_array1.png?raw=true)
## 📝 Parameters
name|optional|description
---|---|------
input_grid|❎|vtk grid
input_code|❎|can be one of these:
||python code|evaluate the code against the grid data
||existing filename|read the content of a .py file as code
||-|for command line piping. reads standard input as code.
output|☑️|path to save the result. if blank input is updated.

## 📓 Notes
## 📚 Examples
### create a new mass cell data from volume and density  
`mass = volume * density`  
### calculate density from lito text  
`density = np.choose(((lito == 'AA') * 1) + ((lito == 'BB') * 2) + ((lito == 'CC') * 3)+ ((lito == 'DD') * 4), (np.nan, 1, 2, 3, 4))`
result will be:  
lito|density
---|---
AA|1
BB|2
CC|3
DD|4
<unknown>|NaN

## 🧩 Compatibility
distribution|status
---|---
![winpython_icon](https://github.com/pemn/assets/blob/main/winpython_icon.png?raw=true)|✔
![vulcan_icon](https://github.com/pemn/assets/blob/main/vulcan_icon.png?raw=true)|❌
![anaconda_icon](https://github.com/pemn/assets/blob/main/anaconda_icon.png?raw=true)|❌
## 🙋 Support
Any question or problem contact:
 - paulo.ernesto
## 💎 License
Apache 2.0  
Copyright ![vale_logo_only](https://github.com/pemn/assets/blob/main/vale_logo_only_r.svg?raw=true) Vale 2023
