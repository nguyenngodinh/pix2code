FROM ubuntu:16.04
LABEL maintainer="nguyennd5@viettel.com.vn"

# caffe2 install with cpu support

RUN apt-get update && apt-get install -y --no-install-recommends \
    git python python-pip zip unzip \
    && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/tonybeltramelli/pix2code /pix2code
WORKDIR /pix2code
RUN pip install --upgrade pip
RUN pip install setuptools
RUN pip install -r requirements.txt
WORKDIR /pix2code
#WORKDIR /pix2code/datasets
#RUN zip -F pix2code_datasets.zip --out datasets.zip && unzip datasets.zip
#WORKDIR /pix2code/model
#RUN ./build_datasets.py ../datasets/web/all_data && ./convert_imgs_to_arrays.py ../datasets/web/training_set ../datasets/web/training_features
########## INSTALLATION STEPS #############
