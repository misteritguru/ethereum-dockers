FROM cptobvious/go-ethereum-base

RUN go get -v -u gopkg.in/qml.v1
RUN go get -v -u -d github.com/ethereum/go-ethereum/ethereum
RUN go get -v -u -d github.com/ethereum/go-ethereum/mist
RUN go get -v -u -d github.com/ethereum/serpent-go

RUN cd $GOPATH/src/github.com/ethereum/serpent-go && git submodule update --init
RUN cd $GOPATH/src/github.com/ethereum/serpent-go && go install -v

RUN cd $GOPATH/src/github.com/ethereum/go-ethereum
RUN cd $GOPATH/src/github.com/ethereum/eth-go

RUN cd $GOPATH/src/github.com/ethereum/go-ethereum/ethereum && go install -v
RUN cd $GOPATH/src/github.com/ethereum/go-ethereum/mist && go install -v

