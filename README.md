## PREDICTv3 R package

The PREDICTv3 R package is a latestly updated PREDICT tool designed to enhance breast cancer prognosis by providing clinicians and researchers with an advanced predictive model. Building upon the foundation of previous iterations, PREDICTv3 integrates a comprehensive set of clinical variables—including patient demographics, tumor characteristics, and treatment modalities—to offer accurate survival predictions tailored to individual patients. PREDICTv3 further enables users to assess the potential benefits and harms of various treatment options, facilitating personalized care strategies. This package aims to support informed decision-making in clinical practice and contribute to ongoing research in oncology.

### Installation

``` r
install.packages("devtools")
library(devtools)
install_github("pengpclab/PREDICTv3")
library(PREDICTv3)
```

### Example code

``` r
data(toyData)
year <- toyData[1, 'year']
age <- toyData[1, 'age']
smoker <- toyData[1, 'smoker']
er <- toyData[1,'er']
pr <- toyData[1, 'pr']
her2 <- toyData[1, 'her2']
ki67 <- toyData[1, 'ki67']
size <- toyData[1, 'size']
grade <- toyData[1, 'grade']
screen <- toyData[1, 'screen']
nodes <- toyData[1, 'nodes']
radio <- toyData[1, 'radio']
heart.gy <- toyData[1, 'heart_gy']
horm <- toyData[1, 'horm']
gen <- toyData[1, 'gen']
traz <- toyData[1, 'traz']
bis <- toyData[1, 'bis']
censor <- 10
PREDICTv3(year=year,
          age=age,
          screen=screen,
          size=size,
          grade=grade,
          nodes=nodes,
          er=er,
          her2=her2,
          ki67=ki67,
          pr=pr,
          radio=radio,
          heart.gy=heart.gy,
          horm=horm,
          gen=gen,
          traz=traz,
          bis=bis,
          smoker = smoker,
          censor=censor)
```

### Citation
Grootes, I., Wishart, G.C. and Pharoah, P.D.P., 2024. An updated PREDICT breast cancer prognostic model including the benefits and harms of radiotherapy. NPJ Breast Cancer, 10(1), p.6.

### Web link
https://breast.predict.cam/

### Authors
Yi-Wen Hsiao (Cedars-Sinai Medical Center, West Hollywood, CA, USA)

Gordon C. Wishart (Anglia Ruskin University, Cambridge, UK)

Paul D.P. Pharoah (Cedars-Sinai Medical Center, West Hollywood, CA, USA)

Pei-Chen Peng (Cedars-Sinai Medical Center, West Hollywood, CA, USA)
