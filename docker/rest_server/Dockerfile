FROM ubuntu:18.04
RUN apt-get update -y
RUN apt-get install gcc g++ cmake git sudo libssl-dev zlib1g-dev -y
RUN apt-get clean -y
RUN git clone -b master https://github.com/pocoproject/poco.git && cd poco && mkdir cmake-build && cd cmake-build && cmake .. && cmake --build . --config Release && cmake --build . --target install && cd .. && rm -r /poco/*
RUN git clone https://github.com/xentellion/arch_lab_2.git && mkdir CMakeFiles && cd CMakeFiles && cmake .. && cmake --build . --config Release && mkdir content && cp ../content/* content/ && cd .. && chmod +x start.sh
ENV LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH