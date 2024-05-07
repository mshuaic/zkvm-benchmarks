# zkVM Benchmarks

## Installation
### Install Jolt
```bash
rustup target add riscv32i-unknown-none-elf
```

### Install Risc Zero
```bash
cargo install cargo-binstall
cargo binstall cargo-risczero
cargo risczero install
```

### Install SP1
```bash
curl -L https://sp1.succinct.xyz | bash
```

Follow the instructions outputted by this command then run:
```bash
sp1up
```

## Running
To run all benchmarks run:
```bash
make bench-all
```

The benchmark results should be outputted in CSV form in `benchmark_outputs`.

To run an individual benchmark run `make bench-jolt`, `make bench-risczero` or `make bench-sp1`.

## testbed specification
- AMD Ryzen 7 5800X 8-Core @ 16x 3.8GHz CPU with 100 GB RAM in WSL2 Ubuntu 22.04.3 LTS in Windows version: 10.0.22631.3447
- SP1 version commit: 10cc576 @2024-05-06
- Risc0 verison: v0.21.0 @2024-03-12
- Jolt version commit: 58d3f7ff614e5cd716310d27bab2c05ef3a847c2 @2024-04-09


## Disclaimer

*This code is being provided as is. No guarantee, representation or warranty is being made, express or implied, as to the safety or correctness of the code. It has not been audited and as such there can be no assurance it will work as intended, and users may experience delays, failures, errors, omissions or loss of transmitted information. Nothing in this repo should be construed as investment advice or legal advice for any particular facts or circumstances and is not meant to replace competent counsel. It is strongly advised for you to contact a reputable attorney in your jurisdiction for any questions or concerns with respect thereto. a16z is not liable for any use of the foregoing, and users should proceed with caution and use at their own risk. See a16z.com/disclosures for more info.*
