# biospy2018
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
