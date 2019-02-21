# BILSTM-CRF
NER|基于Boson数据集

采用的训练集数据是玻森数据提供的命名实体识别数据，可以在https://bosonnlp.com/的数据集里下载，或者直接用BosonNLP_NER_6C.txt

原始数据如下：

{{product_name:浙江在线杭州}}{{time:4月25日}}讯（记者{{person_name: 施宇翔}} 通讯员 {{person_name:方英}}）毒贩很“时髦”，用{{product_name:微信}}交易毒品。没料想警方也很“潮”，将计就计，一举将其擒获。记者从{{org_name:杭州江干区公安分局}}了解到，经过一个多月的侦查工作，{{org_name:江干区禁毒专案组}}抓获吸贩毒人员5名，缴获“冰毒”400余克，毒资30000余元，扣押汽车一辆。

使用data_prepare.ipynb准备数据，主要基于字标记出：B | 词首、M | 词中、E | 词尾、O | 单字

如：浙/B_product_name 江/M_product_name 在/M_product_name 线/M_product_name 杭/M_product_name 州/E_product_name 4/B_time 月/M_time 2/M_time 5/M_time 日/E_time 讯/O

用Train.ipynb的run(2)实现的输出为：

![image](https://github.com/TomatoTang/BILSTM-CRF/blob/master/image/image1.png)
      

