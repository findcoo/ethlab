## ethlab

### 개요 ###
dapp 개발을 위한 다양한 시도들

### dapp ###
* dapp은 솔리디티 패키지 관리자
* 설치법
``` bash
wget https://github.com/dapphub/ethrun/releases/download/v0.2.4/ethrun-v0.2.4-linux.tar.gz
curl https://nixos.org/nix/install | sh
nix-channel --add https://nix.dapphub.com/pkgs/dapphub
nix-channel --update
nix-env -i seth solc
git clone https://github.com/dapphub/dapp
make link -C dapp
```
nix 패키지 관리자를 사용하여 의존성을 모두 설치한다.
* 사용법
``` bash
dapp init # solidity project의 skel 생성, 개발에 필요한 빌드 및 테스트 라이브러리를 포함
dapp install ds-auth # 라이브러리 설치
```
전반적으로 npm과 비슷하다. Makefile, Dappfile을 통해 설정한다.