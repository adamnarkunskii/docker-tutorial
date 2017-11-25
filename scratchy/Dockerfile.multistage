FROM golang as build

RUN mkdir -p /src/scratchy
COPY skkrt.go /src/scratchy

WORKDIR /src/scratchy
RUN go build


FROM scratch

COPY --from=build /src/scratchy/scratchy /scratchy

CMD ["/scratchy"]
