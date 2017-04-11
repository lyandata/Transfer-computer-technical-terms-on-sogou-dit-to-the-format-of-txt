# Transfer-computer-technical-terms-on-sogou-dit-to-the-format-of-txt
When we need to do text analysis,build a technical dictionary is preferred. 

 #安装搜狗字典后将.scel形式转化为.txt
packages1<-c("devtools","stringi","pbapply","Rcpp","RcppProgress")
install.packages("packages1")
install_github("qinwf/cidian")  #在github上下载R中的包
library(devtools);library(stringi);library(pbapply);library(Rcpp);library(RcppProgress)
#以上可用向量的方式下载
library(cidian)
dir.path<-"E:/R/计算机词汇大全【官方推荐】.scel"
#install.packages("stringr")#中有str_C()
#library(stringr)
decode_scel(scel = dir.path,output=paste0(path,".txt"),cpp=TRUE,progress=TRUE) #scel细胞词库的路径，ouput输出文件的路径，cpp加快速度的
