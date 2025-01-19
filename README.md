# weaviate_synopsis
imdb 영화 synopsis data를 weaviate 벡터 db 구축

## 실행환경

### weaviate
* 도커 실행
```
docker run -d \
  -p 8080:8080 \
  -p 50051:50051 \
  -e ENABLE_MODULES='text2vec-openai' \
  -e DEFAULT_VECTORIZER_MODULE='text2vec-openai' \
  -e OPENAI_APIKEY="<YOUR_OPENAI_APIKEY>" \
  -v weaviate_data:/data \
  semitechnologies/weaviate:stable-v1.28-8015521
```

* 최근 stable image
```
docker pull semitechnologies/weaviate:stable-v1.28-8015521
```

* docker file weaviate_data 추출
$ docker cp elated_dubinsky:/data wdata