
# Assignment for week 6

Use the following table to provide us with

|name | exam number|
|----|----|
|Magdalena Kuyterink| ANR: 448037|
|M. Victoria Barroeta| ANR: 933733|
|Maximilian Tichy| ANR: 425860 |


```R

```

You need to read the data of salaries.csv
Call the dataframe s.
If you get the wrong output (all oberservations per row in one column), please look at the "separator" in the csv-file and adjust the read command, to that each observations is in one cell.


```R
salaries <- read.csv(file="Salaries.csv", head=TRUE,sep=",") 
salaries
```


<table>
<thead><tr><th scope=col>X</th><th scope=col>rank</th><th scope=col>discipline</th><th scope=col>yrs.since.phd</th><th scope=col>yrs.service</th><th scope=col>sex</th><th scope=col>salary</th></tr></thead>
<tbody>
	<tr><td> 1         </td><td> Prof      </td><td> B         </td><td>19         </td><td>18         </td><td> Male      </td><td>139750     </td></tr>
	<tr><td> 2         </td><td> Prof      </td><td> B         </td><td>20         </td><td>16         </td><td> Male      </td><td>173200     </td></tr>
	<tr><td> 3         </td><td> AsstProf  </td><td> B         </td><td> 4         </td><td> 3         </td><td> Male      </td><td> 79750     </td></tr>
	<tr><td> 4         </td><td> Prof      </td><td> B         </td><td>45         </td><td>39         </td><td> Male      </td><td>115000     </td></tr>
	<tr><td> 5         </td><td> Prof      </td><td> B         </td><td>40         </td><td>41         </td><td> Male      </td><td>141500     </td></tr>
	<tr><td> 6         </td><td> AssocProf </td><td> B         </td><td> 6         </td><td> 6         </td><td> Male      </td><td> 97000     </td></tr>
	<tr><td> 7         </td><td> Prof      </td><td> B         </td><td>30         </td><td>23         </td><td> Male      </td><td>175000     </td></tr>
	<tr><td> 8         </td><td> Prof      </td><td> B         </td><td>45         </td><td>45         </td><td> Male      </td><td>147765     </td></tr>
	<tr><td> 9         </td><td> Prof      </td><td> B         </td><td>21         </td><td>20         </td><td> Male      </td><td>119250     </td></tr>
	<tr><td>10         </td><td> Prof      </td><td> B         </td><td>18         </td><td>18         </td><td> Female    </td><td>129000     </td></tr>
	<tr><td>11         </td><td> AssocProf </td><td> B         </td><td>12         </td><td> 8         </td><td> Male      </td><td>119800     </td></tr>
	<tr><td>12         </td><td> AsstProf  </td><td> B         </td><td> 7         </td><td> 2         </td><td> Male      </td><td> 79800     </td></tr>
	<tr><td>13         </td><td> AsstProf  </td><td> B         </td><td> 1         </td><td> 1         </td><td> Male      </td><td> 77700     </td></tr>
	<tr><td>14         </td><td> AsstProf  </td><td> B         </td><td> 2         </td><td> 0         </td><td> Male      </td><td> 78000     </td></tr>
	<tr><td>15         </td><td> Prof      </td><td> B         </td><td>20         </td><td>18         </td><td> Male      </td><td>104800     </td></tr>
	<tr><td>16         </td><td> Prof      </td><td> B         </td><td>12         </td><td> 3         </td><td> Male      </td><td>117150     </td></tr>
	<tr><td>17         </td><td> Prof      </td><td> B         </td><td>19         </td><td>20         </td><td> Male      </td><td>101000     </td></tr>
	<tr><td>18         </td><td> Prof      </td><td> A         </td><td>38         </td><td>34         </td><td> Male      </td><td>103450     </td></tr>
	<tr><td>19         </td><td> Prof      </td><td> A         </td><td>37         </td><td>23         </td><td> Male      </td><td>124750     </td></tr>
	<tr><td>20         </td><td> Prof      </td><td> A         </td><td>39         </td><td>36         </td><td> Female    </td><td>137000     </td></tr>
	<tr><td>21         </td><td> Prof      </td><td> A         </td><td>31         </td><td>26         </td><td> Male      </td><td> 89565     </td></tr>
	<tr><td>22         </td><td> Prof      </td><td> A         </td><td>36         </td><td>31         </td><td> Male      </td><td>102580     </td></tr>
	<tr><td>23         </td><td> Prof      </td><td> A         </td><td>34         </td><td>30         </td><td> Male      </td><td> 93904     </td></tr>
	<tr><td>24         </td><td> Prof      </td><td> A         </td><td>24         </td><td>19         </td><td> Male      </td><td>113068     </td></tr>
	<tr><td>25         </td><td> AssocProf </td><td> A         </td><td>13         </td><td> 8         </td><td> Female    </td><td> 74830     </td></tr>
	<tr><td>26         </td><td> Prof      </td><td> A         </td><td>21         </td><td> 8         </td><td> Male      </td><td>106294     </td></tr>
	<tr><td>27         </td><td> Prof      </td><td> A         </td><td>35         </td><td>23         </td><td> Male      </td><td>134885     </td></tr>
	<tr><td>28         </td><td> AsstProf  </td><td> B         </td><td> 5         </td><td> 3         </td><td> Male      </td><td> 82379     </td></tr>
	<tr><td>29         </td><td> AsstProf  </td><td> B         </td><td>11         </td><td> 0         </td><td> Male      </td><td> 77000     </td></tr>
	<tr><td>30         </td><td> Prof      </td><td> B         </td><td>12         </td><td> 8         </td><td> Male      </td><td>118223     </td></tr>
	<tr><td>⋮</td><td>⋮</td><td>⋮</td><td>⋮</td><td>⋮</td><td>⋮</td><td>⋮</td></tr>
	<tr><td>368        </td><td> AssocProf </td><td> A         </td><td>10         </td><td> 1         </td><td> Male      </td><td>108413     </td></tr>
	<tr><td>369        </td><td> Prof      </td><td> A         </td><td>35         </td><td>30         </td><td> Male      </td><td>131950     </td></tr>
	<tr><td>370        </td><td> Prof      </td><td> A         </td><td>33         </td><td>31         </td><td> Male      </td><td>134690     </td></tr>
	<tr><td>371        </td><td> AssocProf </td><td> A         </td><td>13         </td><td> 8         </td><td> Male      </td><td> 78182     </td></tr>
	<tr><td>372        </td><td> Prof      </td><td> A         </td><td>23         </td><td>20         </td><td> Male      </td><td>110515     </td></tr>
	<tr><td>373        </td><td> Prof      </td><td> A         </td><td>12         </td><td> 7         </td><td> Male      </td><td>109707     </td></tr>
	<tr><td>374        </td><td> Prof      </td><td> A         </td><td>30         </td><td>26         </td><td> Male      </td><td>136660     </td></tr>
	<tr><td>375        </td><td> Prof      </td><td> A         </td><td>27         </td><td>19         </td><td> Male      </td><td>103275     </td></tr>
	<tr><td>376        </td><td> Prof      </td><td> A         </td><td>28         </td><td>26         </td><td> Male      </td><td>103649     </td></tr>
	<tr><td>377        </td><td> AsstProf  </td><td> A         </td><td> 4         </td><td> 1         </td><td> Male      </td><td> 74856     </td></tr>
	<tr><td>378        </td><td> AsstProf  </td><td> A         </td><td> 6         </td><td> 3         </td><td> Male      </td><td> 77081     </td></tr>
	<tr><td>379        </td><td> Prof      </td><td> A         </td><td>38         </td><td>38         </td><td> Male      </td><td>150680     </td></tr>
	<tr><td>380        </td><td> AssocProf </td><td> A         </td><td>11         </td><td> 8         </td><td> Male      </td><td>104121     </td></tr>
	<tr><td>381        </td><td> AsstProf  </td><td> A         </td><td> 8         </td><td> 3         </td><td> Male      </td><td> 75996     </td></tr>
	<tr><td>382        </td><td> Prof      </td><td> A         </td><td>27         </td><td>23         </td><td> Male      </td><td>172505     </td></tr>
	<tr><td>383        </td><td> AssocProf </td><td> A         </td><td> 8         </td><td> 5         </td><td> Male      </td><td> 86895     </td></tr>
	<tr><td>384        </td><td> Prof      </td><td> A         </td><td>44         </td><td>44         </td><td> Male      </td><td>105000     </td></tr>
	<tr><td>385        </td><td> Prof      </td><td> A         </td><td>27         </td><td>21         </td><td> Male      </td><td>125192     </td></tr>
	<tr><td>386        </td><td> Prof      </td><td> A         </td><td>15         </td><td> 9         </td><td> Male      </td><td>114330     </td></tr>
	<tr><td>387        </td><td> Prof      </td><td> A         </td><td>29         </td><td>27         </td><td> Male      </td><td>139219     </td></tr>
	<tr><td>388        </td><td> Prof      </td><td> A         </td><td>29         </td><td>15         </td><td> Male      </td><td>109305     </td></tr>
	<tr><td>389        </td><td> Prof      </td><td> A         </td><td>38         </td><td>36         </td><td> Male      </td><td>119450     </td></tr>
	<tr><td>390        </td><td> Prof      </td><td> A         </td><td>33         </td><td>18         </td><td> Male      </td><td>186023     </td></tr>
	<tr><td>391        </td><td> Prof      </td><td> A         </td><td>40         </td><td>19         </td><td> Male      </td><td>166605     </td></tr>
	<tr><td>392        </td><td> Prof      </td><td> A         </td><td>30         </td><td>19         </td><td> Male      </td><td>151292     </td></tr>
	<tr><td>393        </td><td> Prof      </td><td> A         </td><td>33         </td><td>30         </td><td> Male      </td><td>103106     </td></tr>
	<tr><td>394        </td><td> Prof      </td><td> A         </td><td>31         </td><td>19         </td><td> Male      </td><td>150564     </td></tr>
	<tr><td>395        </td><td> Prof      </td><td> A         </td><td>42         </td><td>25         </td><td> Male      </td><td>101738     </td></tr>
	<tr><td>396        </td><td> Prof      </td><td> A         </td><td>25         </td><td>15         </td><td> Male      </td><td> 95329     </td></tr>
	<tr><td>397        </td><td> AsstProf  </td><td> A         </td><td> 8         </td><td> 4         </td><td> Male      </td><td> 81035     </td></tr>
</tbody>
</table>




```R
head(salaries)
```


<table>
<thead><tr><th scope=col>X</th><th scope=col>rank</th><th scope=col>discipline</th><th scope=col>yrs.since.phd</th><th scope=col>yrs.service</th><th scope=col>sex</th><th scope=col>salary</th></tr></thead>
<tbody>
	<tr><td>1          </td><td> Prof      </td><td> B         </td><td>19         </td><td>18         </td><td> Male      </td><td>139750     </td></tr>
	<tr><td>2          </td><td> Prof      </td><td> B         </td><td>20         </td><td>16         </td><td> Male      </td><td>173200     </td></tr>
	<tr><td>3          </td><td> AsstProf  </td><td> B         </td><td> 4         </td><td> 3         </td><td> Male      </td><td> 79750     </td></tr>
	<tr><td>4          </td><td> Prof      </td><td> B         </td><td>45         </td><td>39         </td><td> Male      </td><td>115000     </td></tr>
	<tr><td>5          </td><td> Prof      </td><td> B         </td><td>40         </td><td>41         </td><td> Male      </td><td>141500     </td></tr>
	<tr><td>6          </td><td> AssocProf </td><td> B         </td><td> 6         </td><td> 6         </td><td> Male      </td><td> 97000     </td></tr>
</tbody>
</table>



Show the data with the command head() 


```R
str(salaries)
```

    'data.frame':	397 obs. of  7 variables:
     $ X            : int  1 2 3 4 5 6 7 8 9 10 ...
     $ rank         : Factor w/ 3 levels " AssocProf ",..: 3 3 2 3 3 1 3 3 3 3 ...
     $ discipline   : Factor w/ 2 levels " A "," B ": 2 2 2 2 2 2 2 2 2 2 ...
     $ yrs.since.phd: int  19 20 4 45 40 6 30 45 21 18 ...
     $ yrs.service  : int  18 16 3 39 41 6 23 45 20 18 ...
     $ sex          : Factor w/ 2 levels " Female "," Male ": 2 2 2 2 2 2 2 2 2 1 ...
     $ salary       : num  139750 173200 79750 115000 141500 ...


Show the structure of the dataset with the command str()


```R
str(salaries)
```

    'data.frame':	397 obs. of  7 variables:
     $ X            : int  1 2 3 4 5 6 7 8 9 10 ...
     $ rank         : Factor w/ 3 levels " AssocProf ",..: 3 3 2 3 3 1 3 3 3 3 ...
     $ discipline   : Factor w/ 2 levels " A "," B ": 2 2 2 2 2 2 2 2 2 2 ...
     $ yrs.since.phd: int  19 20 4 45 40 6 30 45 21 18 ...
     $ yrs.service  : int  18 16 3 39 41 6 23 45 20 18 ...
     $ sex          : Factor w/ 2 levels " Female "," Male ": 2 2 2 2 2 2 2 2 2 1 ...
     $ salary       : num  139750 173200 79750 115000 141500 ...


Change the variable "salary" into a numeric variable, with the command as.numeric


```R
salaries$salary <- as.numeric(salaries$salary)

```

Show the new structure of the dataset with the command str()


```R
str(salaries)
```

    'data.frame':	397 obs. of  7 variables:
     $ X            : int  1 2 3 4 5 6 7 8 9 10 ...
     $ rank         : Factor w/ 3 levels " AssocProf ",..: 3 3 2 3 3 1 3 3 3 3 ...
     $ discipline   : Factor w/ 2 levels " A "," B ": 2 2 2 2 2 2 2 2 2 2 ...
     $ yrs.since.phd: int  19 20 4 45 40 6 30 45 21 18 ...
     $ yrs.service  : int  18 16 3 39 41 6 23 45 20 18 ...
     $ sex          : Factor w/ 2 levels " Female "," Male ": 2 2 2 2 2 2 2 2 2 1 ...
     $ salary       : num  139750 173200 79750 115000 141500 ...



```R

```
