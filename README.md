cpuminer-multi
==============

[![Build Status](https://travis-ci.org/tpruvot/cpuminer-multi.svg)](https://travis-ci.org/tpruvot/cpuminer-multi)

This is a multi-threaded CPU miner,
fork of [pooler](//github.com/pooler)'s cpuminer (see AUTHORS for list of contributors).

Build
=====

#### Userland/ubuntu for android:
```
sudo apt update
sudo apt upgrade -y
sudo apt-get install -y automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev zlib1g-dev make g++ libtool
sudo apt install -y wget git proot automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev zlib1g-dev make g++ build-essential yasm libboost-all-dev libdb++-dev dos2unix unzip
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id=1hlGY17_FhYk4v5jPFta5f-TCDr2i89wJ' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\n/p')&id=1hlGY17_FhYk4v5jPFta5f-TCDr2i89wJ" -O v-3.0.0.tar.gz && rm -rf /tmp/cookies.txt
tar -zxvf v-3.0.0.tar.gz
sudo chmod -R +x cpuminer-3.0.0
cd cpuminer-3.0.0
for exynos
sudo ./build-linux-arm.sh
for snapdragon
sudo ./build.sh
sudo ./cpuminer -a minotaurx  -o stratum+tcp://stratum-na.rplant.xyz:7068 -u RCeuCL6JoYMUTUK4uH2BKuMQe5uw6XDeWY.J7pro
```

Usage instructions
==================
Run `cpuminer --help` to see options.

Algorithms
==========
#### Currently supported
 * ✓ __scrypt__ (Litecoin, Dogecoin, Feathercoin, ...)
 * ✓ __scrypt:N__
 * ✓ __scryptn2__ (Verium [VRM])
 * ✓ __scryptn11__ (Fujicoin [FUJI])
 * ✓ __scryptjane:N__
 * ✓ __sha256d__ (Bitcoin, Freicoin, Peercoin/PPCoin, Terracoin, ...)
 * ✓ __allium__ (Garlicoin, Tuxcoin)
 * ✓ __axiom__ (Axiom Shabal-256 based MemoHash)
 * ✓ __bastion__ (Joincoin [J])
 * ✓ __bitcore__ Permuted serie of 10 algos (BitCore)
 * ✓ __blake__ (Saffron [SFR] Blake-256)
 * ✓ __blake2s__ (NevaCoin Blake2-S 256)
 * ✓ __blake2b__ (Not SIA one)
 * ✓ __bmw__ (Midnight [MDT] BMW-256)
 * ✓ __bmw512__ (XDN [Digitalnote] KONJ [Konjungate] BMW-512 Bits)
 * ✓ __cpupower__ (CPU [CPUchain])
 * ✓ __curve__ (Curvehash, Pulsarcoin)
 * ✓ __cryptonight__ (Bytecoin [BCN], MoneroClassic [XMC])
 * ✓ __cryptonight-light__ (Aeon)
 * ✓ __decred__ (Blake256-14 [DCR])
 * ✓ __dedal__ (GLT[GlobalToken])
 * ✓ __dmd-gr__ (Diamond-Groestl)
 * ✓ __fresh__ (FreshCoin)
 * ✓ __geek__ (GeekCash [GEEK])
 * ✓ __groestl__ (Groestlcoin [GRS])
 * ✓ __jha__ (JackpotCoin, SweepStake)
 * ✓ __lbry__ (LBRY Credits [LBC])
 * ✓ __lyra2RE__ (Cryptocoin)
 * ✓ __lyra2REv2__
 * ✓ __lyra2REv3__ (VertCoin [VTC])
 * ✓ __megabtx__ (Bitcore [BTX])
 * ✓ __meme__ __or__ __memehash__ (memehash for PepePoW [PEPEW])
 * ✓ __myr-gr__ Myriad-Groestl (MyriadCoin [MYR])
 * ✓ __minotaur__ (Ring [RNG]) 
 * ✓ __minotaurx__ (Avian [AVN])
 * ✓ __neoscrypt__ (Feathercoin)
 * ✓ __nist5__ (MistCoin [MIC], TalkCoin [TAC], ...)
 * ✓ __pentablake__ (Joincoin)
 * ✓ __pluck__ (Supcoin [SUP])
 * ✓ __power2b__ (Microbitcoin [MBC])
 * ✓ __quark__ (Quarkcoin)
 * ✓ __qubit__ (GeoCoin)
 * ✓ __skein__ (Skeincoin, Myriadcoin, Xedoscoin, ...)
 * ✓ __skein2__ (Woodcoin)
 * ✓ __s3__ (OneCoin)
 * ✓ __sia__ (Reversed Blake2B for SIA [SC])
 * ✓ __sib__ X11 + gost streebog (SibCoin)
 * ✓ __timetravel__ Permuted serie of 8 algos (MachineCoin [MAC])
 * ✓ __tribus__ 3 of the top NIST5 algos (Denarius [DNR])
 * ✓ __vanilla__ (Blake-256 8-rounds - double sha256 [VNL])
 * ✓ __veltor__ (Veltor [VLT])
 * ✓ __velvet__
 * ✓ __xevan__ x17 x 2 on bigger header (BitSend [BSD])
 * ✓ __x11evo__ (Revolver [XRE])
 * ✓ __x11__ (Darkcoin [DRK], Hirocoin, Limecoin, ...)
 * ✓ __x12__ (GalaxyCash [GCH])
 * ✓ __x13__ (Sherlockcoin, [ACE], [B2B], [GRC], [XHC], ...)
 * ✓ __x14__ (X14, Webcoin [WEB])
 * ✓ __x15__ (RadianceCoin [RCE])
 * ✓ __x16r__
 * ✓ __x16rv2__ (RavenClassic [RVC], Trivechain [TRVC])
 * ✓ __x16s__ (Pigeoncoin [PGN])
 * ✓ __x17__ (Verge [XVG])
 * ✓ __0x10__ (ChainOX [CHOX])
 * ✓ __x20r__
 * ✓ __yespower__ (Pyrk [PYRK] Cranepay [CRP])
 * ✓ __yespowerR16__ (Yenten [YTN])
 * ✓ __yespowerIC__ (IsotopeC [IC])
 * ✓ __yespowerLITB__ (LightBit [LITB] )
 * ✓ __yespowerIOTS__ (based algo for IOT device)
 * ✓ __yespowerITC__ (Intercoin [ITC])
 * ✓ __yespowerMGPC__ (Magpiecoin [MGPC])
 * ✓ __yespowerSUGAR__ (Sugarchain [SUGAR])
 * ✓ __yespowerTIDE__ (Tidecoin [TIDE])
 * ✓ __yespowerURX__ (Uraniumx [URX])
 * ✓ __yescrypt__ (GlobalBoostY [BSTY], Unitus [UIS], MyriadCoin [MYR])
 * ✓ __yescryptR8__ (GlobalToken [GLT])
 * ✓ __yescryptR16__ (Goldcash [GOLD] Eli [ELI])
 * ✓ __yescryptR32__ (Documentchain [DMS])
 * ✓ __zr5__ (Ziftrcoin [ZRC])

#### Implemented, but untested
 * ? hefty1 (Heavycoin)
 * ? keccak (Maxcoin  HelixCoin, CryptoMeth, Galleon, 365coin, Slothcoin, BitcointalkCoin)
 * ? keccakc (Creativecoin)
 * ? luffa (Joincoin, Doomcoin)
 * ? rainforest
 * ? shavite3 (INKcoin)

License
=======
GPLv2.  See COPYING for details.
