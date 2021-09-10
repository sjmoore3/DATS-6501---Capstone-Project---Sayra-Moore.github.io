# DATS 6501 - Capstone Project - Sayra Moore

Welcome to my github site, where you will find my commented code for my capstone project! The purpose of this project was to focus on determining if a person would fall victim to a cybercrime when taking into consideration

# Code

```markdown
cyber <- read.csv(file = "C:/Users/ipcon/OneDrive - The George Washington University/Summer 2021/DATS 6501/DATS 6501 - Capstone Project - Sayra Moore/Cybercrime_Dataset Clean_CSV.csv")
str(cyber)

summary(cyber)
```

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)

## Correlation
``` 
cor.test(cyber$Age,cyber$No_Cyber_Atks_1mo,method = "pearson")
plot(cyber$Age,cyber$No_Cyber_Atks_1mo)
#Figure1
```
``` 
cor.test(cyber$Sess_Cnt_1mos,cyber$No_Cyber_Atks_1mo,method="pearson")
plot(cyber$Sess_Cnt_1mos,cyber$No_Cyber_Atks_1mo)
#Figure2
```
## Data Cleansing
### Cleaning the "CC_Fraud" variable:
```
cyber$CC_Fraud <- gsub("No",0,cyber$CC_Fraud)
cyber$CC_Fraud <- as.integer(cyber$CC_Fraud)
```

### Cleaning the "Date of Attack" variable:
```
cyber$Date.of.Attack <- as.Date(cyber$Date.of.Attack,format="%m/%d/%Y")
```

### Cleaning the "Computer" variable:
```
cyber$Computer <- gsub("No",0,cyber$Computer)
cyber$Computer <- gsub("Yes",1,cyber$Computer)
cyber$Computer <- as.integer(cyber$Computer)
```

### Cleaning the "Tablet" variable:
```
cyber$Tablet <- gsub("No",0,cyber$Tablet)
cyber$Tablet <- gsub("Yes",1,cyber$Tablet)
cyber$Tablet <- as.integer(cyber$Tablet)
```

### Cleaning the "Cell_Phone" variable:
```
cyber$Cell_Phone <- gsub("No",0,cyber$Cell_Phone)
cyber$Cell_Phone <- gsub("Yes",1,cyber$Cell_Phone)
cyber$Cell_Phone <- as.integer(cyber$Cell_Phone)
```

### Cleaning the "Social_Net" variable:
```
cyber$Social_Net <- gsub("No",0,cyber$Social_Net)
cyber$Social_Net <- gsub("Yes",1,cyber$Social_Net)
cyber$Social_Net <- as.integer(cyber$Social_Net)
```

### Cleaning the "Malware.Present variable:
```
cyber$Malware.Present <- gsub("No",0,cyber$Malware.Present)
cyber$Malware.Present <- gsub("Yes",1,cyber$Malware.Present)
cyber$Malware.Present <- as.integer(cyber$Malware.Present)
```
For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/sjmoore3/DATS-6501---Capstone-Project---Sayra-Moore.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
