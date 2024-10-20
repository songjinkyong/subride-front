FROM nginx:1.26-alpine3.19-otel

## 파이프라인에서 빌드된 결과물을 nginx의 샘플 앱이 사용하던 폴더로 복사
COPY ./build /usr/share/nginx/html

## nginx 설정 파일 복사
COPY ./deployment/default.conf.template /etc/nginx/conf.d/default.conf

## 80포트 오픈하고 nginx 실행
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]