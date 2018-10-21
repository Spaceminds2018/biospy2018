# biospy2018
title: "Breathing Rate of Subjects A,B,C"
runtime: shiny
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
breathing_rate_neurospyA<-head(read.table("/Users/athulyaajith/Desktop/breathing_rate-neurospyA.csv", sep=","),1000)
breathing_rate_neurospyB<-head(read.table("/Users/athulyaajith/Desktop/breathing_rate-neurospyB.csv", sep=","),1000)
breathing_rate_neurospyC<-head(read.table("/Users/athulyaajith/Desktop/breathing_rate-neurospyC.csv", sep=","),1000)
breathing_rate_neurospyA<-breathing_rate_neurospyA[-1,]
breathing_rate_neurospyB<-breathing_rate_neurospyB[-1,]
breathing_rate_neurospyC<-breathing_rate_neurospyC[-1,]
require(ggplot2)
require(plotly)
```

#Subject A
```{r, echo=FALSE, include = TRUE}

BaseLayerA<-ggplot(data = breathing_rate_neurospyA, 
                   aes(x=as.numeric(V1), y = as.numeric(V2)))+
  ylab("Breathing Rate(rpm)")+
  xlab("time(s/1000)")
ggplotly(BaseLayerA+geom_line(group=1))

```

#Subject B
```{r, echo=FALSE}

BaseLayerA<-ggplot(data = breathing_rate_neurospyB, aes(x=as.numeric(V1), y = as.numeric(V2)))+
xlab("time(s/1000)")+
  ylab("Breathing Rate(rpm)")
ggplotly(BaseLayerA+geom_line(group=1))

```


#Subject C
```{r, echo=FALSE}

BaseLayerA<-ggplot(data = breathing_rate_neurospyC, aes(x=as.numeric(V1), y = as.numeric(V2)))+
xlab("time(s/1000)")+
ylab("Breathing Rate(rpm)")
ggplotly(BaseLayerA+geom_line(group=1))

```

title: "Heart Rate of Subjects A,B,C"
runtime: shiny
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
heart_rate_neurospyA<-head(read.table("/Users/athulyaajith/Desktop/heart_rate-neurospyA.csv", sep=","),1000)
heart_rate_neurospyB<-head(read.table("/Users/athulyaajith/Desktop/heart_rate-neurospyB.csv", sep=","),1000)
heart_rate_neurospyC<-head(read.table("/Users/athulyaajith/Desktop/heart_rate-neurospyC.csv", sep=","),1000)
heart_rate_neurospyA<-heart_rate_neurospyA[-1,]
heart_rate_neurospyB<-heart_rate_neurospyB[-1,]
heart_rate_neurospyC<-heart_rate_neurospyC[-1,]
require(ggplot2)
require(plotly)
```
#Subject A
```{r echo=FALSE, include=TRUE}

BaseLayerA<-ggplot(data = heart_rate_neurospyA, 
                   aes(x=as.numeric(V1),y = as.numeric(V2)))+
  ylab("Heart Rate(bpm)") +
  xlab("time(s/1000)")
ggplotly(BaseLayerA+geom_line(group=1))

```
#Subject B

```{r echo=FALSE}

BaseLayerA<-ggplot(data = heart_rate_neurospyB, 
                   aes(x=as.numeric(V1), y = as.numeric(V2)))+
  ylab("Heart Rate(bpm)") +
  xlab("time(s/1000)")
ggplotly(BaseLayerA+geom_line(group=1))

```
#Subject C

```{r echo=FALSE}

BaseLayerA<-ggplot(data = heart_rate_neurospyC, 
                   aes(x=as.numeric(V1), y = as.numeric(V2)))+
  ylab("Heart Rate(bpm)")+
xlab("time(s/1000)")
ggplotly(BaseLayerA+geom_line(group=1))

```
```
title: "Systolic Pressure of Subjects A,B,C"
runtime: shiny
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
systolic_pressure_neurospyA<-head(read.table("/Users/athulyaajith/Desktop/systolic_pressure_neurospyA.csv", sep=","),1000)
systolic_pressure_neurospyB<-head(read.table("/Users/athulyaajith/Desktop/systolic_pressure_neurospyB.csv", sep=","),1000)
systolic_pressure_neurospyC<-head(read.table("/Users/athulyaajith/Desktop/systolic_pressure_neurospyC.csv", sep=","),1000)
systolic_pressure_neurospyA<-systolic_pressure_neurospyA[-1,]
systolic_pressure_neurospyB<-systolic_pressure_neurospyB[-1,]
systolic_pressure_neurospyC<-systolic_pressure_neurospyC[-1,]
require(ggplot2)
require(plotly)
```
#Subject A
```{r echo=FALSE, include=TRUE}

BaseLayerA<-ggplot(data = systolic_pressure_neurospyA, aes(x=as.numeric(V1),y = as.numeric(V2)))+
xlab("time(s/1000)")+
ylab("Systolic Pressure(mmHg)")
ggplotly(BaseLayerA+geom_line(group=1))
```
#Subject B
```{r echo=FALSE}

BaseLayerA<-ggplot(data = systolic_pressure_neurospyB, aes(x=as.numeric(V1),y = as.numeric(V2)))+
  xlab("time(s/1000)")+
  ylab("Systolic Pressure(mmHg)")
ggplotly(BaseLayerA+geom_line(group=1))
```
#Subject C
```{r echo=FALSE}

BaseLayerA<-ggplot(data = systolic_pressure_neurospyC, aes(x=as.numeric(V1),y= as.numeric(V2)))+
  xlab("time(s/1000)")+
  ylab("Systolic Pressure(mmHg)")
ggplotly(BaseLayerA+geom_line(group=1))

```
