# ������� 2 ������� ������ R
```{r}
Males<-data.frame(
        Sex=rep('Male', 50),
        Tail=rnorm(50, 50, 10))
Males

Females<-data.frame(
        Sex=rep('Female', 50),
        Tail=rnorm(50, 40, 10))
Swifts<-rbind(Males, Females)

Swifts

head(Swifts, 10)

tail(Swifts)

str(Swifts)

ls() # ����������� ������� � ������

?ls

Swifts[ 1:10, 2] # � ������ �� ������� ������ �� ������ �������

Swifts$Sex
Swifts[,1]

nrow(Swifts) # ����� �������
ncol(Swifts) # ����� ��������

Swifts[nrow(Swifts), ncol(Swifts)]<-40
Swifts$Tail[length(Swifts$Tail)]<-40


Swifts[Swifts$Tail>60,]

Swifts[Swifts$Sex=='Male',]

save(Swifts, file='Swifts.RData')

getwd() # ���������� ������� ����������
setwd('F:/tmp') # ���������� ������� ����������

��������� � ���������� ������� R
```{r}
save(Swifts, file='Swifts.RData')
load('Swifts.RData')
```



��������� .csv ����
```{r}
write.csv2(Swifts, 
      file='Swifts.csv',
      row.names=FALSE)

Swifts<-read.csv2(file='Swifts.csv')
```


install.packages('FLightR')

library('nlme')
citation('nlme')




