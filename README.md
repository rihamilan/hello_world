# hello_world
learning git


```
# This will install actel's development version:
remotes::install_github("hugomflavio/actel",
                        build_opts = c("--no-resave-data", "--no-manual"), 
                        build_vignettes = TRUE)

library("actel")
# The displayed version should now be 1.3.0.9008
# If that is not the case, unload actel and load it again.
# Once you have version 1.3.0.9008 running, you can see the help for the new function with ?convertLotekCDMAFile. Essentially, you need to provide it with the file name, the format of the dates, and the timezone of the study area. The function will return your detections as a data.table object, which you can then save as a csv file and use with actel.

#Something like this:
  
  x <- convertLotekCDMAFile(file = "C:/Prace/jeseter_help/1_dowload_2024/WHS3K-3010043_20240827_070715.TXT",
                            date_format = "%m/%d/%y") # <- change this line
head(x)
write.csv(x, "lotek_log.csv", row.names = FALSE)
```
