# PDAL 使用指南

## 简介

这是我的PDAL学习项目,部分使用输电线路点云文件测试。

## 安装PDAL

### 官方指令

    $ conda env remove -n gisse
    $ conda create -n gisse -c conda-forge pdal python-pdal matplotlib -y
    $ conda activate gisse

### 我的安装

    conda create -n pdal3.5 python=3.5
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --set show_channel_urls yes
    conda install -c conda-forge pdal python-pdal

### 测试命令

    pdal info pdal\exercises\translation\interesting.las -p 0
    pdal translate pdal\exercises\translation\interesting.las interesting.txt
    pdal info --metadata pdal\exercises\translation\interesting.las
    pdal pipeline -i pipeline-yupont.json
    pdal info -p 1-5 r16.las

## 工作记录

### 目录与文件说明

目录或文件|说明
---------|----
docu|文档
workshop|存放点云文件，包括输入、输出
notebook|ipynb文件

## 参考项目

1. f4g-oceania-pdal

非常完备的教学包。
Processing and visualising point clouds with the PDAL/Entwine/Potree stack
A workshop designed for [FOSS4G SotM Oceania 2018](http://fossf4g-oceania.org)

3. learning-pdal

基于容器内pdal+jupyter。
The purpose of this repository is to provide instructions as to how one can get started running PDAL within a Jupyter notebook.

4. pdal-notebook

5. pipelines

Example pipelines and workflows for PDAL

6. pointCloudProcessing

repo for practicing with pdal and plotting in jupyter