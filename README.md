# R-package-installing

#R package installed way
.libPaths()
#R build-in insatlling
install.packages("< package >")
#unload the loading package
detach("package:< package >", unload=TRUE)
#delete package
remove.packages("< package >",lib = file.path(<package pathway>))
#list installed packages
installed.packages()
work<-as.data.frame(installed.packages())
work["< package >",]

#using source core in shell
R CMD INSTALL /mnt/data/user_data/xiangyu/programme/R_PACKAGES/seurat-3.2.3.tar.gz
R CMD INSTALL /mnt/data/user_data/shuhao/program/R/package/Matrix_1.4-0.tar.gz
R CMD INSTALL /mnt/data/user_data/shuhao/program/R/package/Matrix_1.6-0.tar.gz



#using devtools
library("devtools")
#devtools install by source code
devtools::install_local("<package source core pathway>")
#update
devtools::update_packages("< package >")
#install special version package
devtools::install_version("< package >", version = "<vesion>",repos = "<cram>")

#using biomanager

library("BiocManager")
#install BiocManager
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

#searching available package
BiocManager::available("< package >")
#intall package
BiocManager::install("< package >")



