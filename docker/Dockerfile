FROM  pytorch/pytorch:1.12.1-cuda11.3-cudnn8-runtime

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y --no-install-recommends \
        libgl1-mesa-glx \
        libsm6 \
        libxext6 libxrender1 \
    && rm -rf /var/lib/apt/lists.*

WORKDIR /workspace

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .
CMD ["bash"]

