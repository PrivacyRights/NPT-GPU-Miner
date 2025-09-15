# NPT GPU Miner

A high-performance GPU mining software for Neptune Cash (NPT) cryptocurrency, optimized for NVIDIA GPUs with 21GB+ VRAM.

## 🚀 Quick Start

### Prerequisites
- NVIDIA GPU with 21GB+ VRAM
- Linux/Ubuntu system
- Neptune wallet address
- CUDA drivers installed

### Supported GPUs
- **L40S** - 7.0 MN/s
- **RTX 6000 ADA** - 6.5 MN/s  
- **A40** - 3.5 MN/s
- **RTX 5090** - 2.8 MN/s
- **RTX 4090** - 2.1 MN/s

## 📥 Installation

1. **Download the miner binaries**
   ```bash
   # Clone or download the repository
   git clone https://github.com/PrivacyRights/NPT-GPU-Miner.git
   cd NPT-GPU-Miner
   ```

2. **Make the script executable**
   ```bash
   chmod +x run-miner.sh
   ```

3. **Run the miner**
   ```bash
   ./run-miner.sh
   ```

## ⚙️ Binary Selection

Choose the appropriate miner binary based on your GPU:

### High Memory GPUs (42GB+ VRAM)
- **L40S, A40, RTX 6000 ADA**
- Use: `./miner_42g`

### Standard GPUs (21GB+ VRAM)
- **RTX 4090, RTX 5090**
- Use: `./miner_21g`

## 🎯 Usage

### Basic Usage
```bash
# For high memory GPUs
./miner_42g --gpu 0 --guesser-address YOUR_WALLET_ADDRESS

# For standard GPUs  
./miner_21g --gpu 0 --guesser-address YOUR_WALLET_ADDRESS
```

### Multi-GPU Setup
```bash
# Run on multiple GPUs with different nonce offsets
./miner_42g --gpu 0 --nonce-offset 0 --guesser-address YOUR_WALLET_ADDRESS &
./miner_42g --gpu 1 --nonce-offset 150 --guesser-address YOUR_WALLET_ADDRESS &
./miner_42g --gpu 2 --nonce-offset 300 --guesser-address YOUR_WALLET_ADDRESS &
```

### Command Line Options
- `--gpu <id>` - GPU device ID (0, 1, 2, etc.)
- `--nonce-offset <value>` - Nonce offset for multi-GPU setups
- `--guesser-address <address>` - Your Neptune wallet address

## 📊 Performance Benchmarks

| GPU Model | Hashrate | NPT/hour | Power Usage |
|-----------|----------|----------|-------------|
| L40S | 7.0 MN/s | ~30 NPT/h | ~300W |
| RTX 6000 ADA | 6.5 MN/s | ~28 NPT/h | ~300W |
| A40 | 3.5 MN/s | ~15 NPT/h | ~250W |
| RTX 5090 | 2.8 MN/s | ~13 NPT/h | ~450W |
| RTX 4090 | 2.1 MN/s | ~10 NPT/h | ~450W |

*Performance may vary based on system configuration and overclocking.*

## 🔧 System Requirements

### Minimum Requirements
- **OS**: Ubuntu 18.04+ or compatible Linux distribution
- **GPU**: NVIDIA GPU with 21GB+ VRAM
- **RAM**: 32GB system RAM
- **Storage**: 10GB free space
- **CUDA**: Version 11.0 or higher

### Recommended Requirements
- **OS**: Ubuntu 20.04+ or Ubuntu 22.04
- **GPU**: L40S, RTX 6000 ADA, or A40
- **RAM**: 64GB+ system RAM
- **Storage**: SSD with 50GB+ free space
- **CUDA**: Latest version

## 🏊‍♂️ Mining Pools

### Recommended Pools
- **CatsPool** - First NPT GPU mining pool with 0% fees
- **Direct rewards** to miners
- **gRPC architecture** for low latency
- **99.9% uptime** guarantee

### Pool Configuration
```bash
# Example pool connection
./miner_42g --gpu 0 --guesser-address YOUR_WALLET_ADDRESS
```

## 🛠️ Troubleshooting

### Common Issues

**1. CUDA Out of Memory**
```bash
# Check GPU memory
nvidia-smi

# Reduce batch size or use smaller GPU
./miner_21g --gpu 0 --batch-size 1
```

**2. Permission Denied**
```bash
# Make sure script is executable
chmod +x run-miner.sh
chmod +x miner_42g
chmod +x miner_21g
```

**3. GPU Not Detected**
```bash
# Check NVIDIA drivers
nvidia-smi

# Install CUDA if needed
sudo apt update
sudo apt install nvidia-cuda-toolkit
```

**4. Low Hashrate**
- Ensure GPU is not thermal throttling
- Check power limits with `nvidia-smi`
- Verify CUDA version compatibility
- Close other GPU-intensive applications

## 📈 Optimization Tips

### GPU Optimization
- **Power Limit**: Set to 100% or maximum
- **Memory Clock**: Increase by 500-1000 MHz
- **Core Clock**: Increase by 100-200 MHz
- **Temperature**: Keep below 80°C

### System Optimization
- **Disable GUI**: Use headless mode for better performance
- **Close Background Apps**: Free up system resources
- **Use SSD**: Faster storage for better performance
- **Adequate Cooling**: Ensure proper ventilation

## 🔒 Security

### Wallet Security
- **Never share** your private keys
- **Use hardware wallets** for large amounts
- **Keep software updated** regularly
- **Verify downloads** with checksums

### System Security
- **Firewall**: Configure proper firewall rules
- **Updates**: Keep system and drivers updated
- **Monitoring**: Monitor system resources and temperatures

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/PrivacyRights/NPT-GPU-Miner/issues)
- **Discussions**: [GitHub Discussions](https://github.com/PrivacyRights/NPT-GPU-Miner/discussions)
- **Twitter**: [@Catzpool](https://x.com/Catzpool)
- **Telegram**: [CatsPool Community](https://t.me/catzpool)
- **Discord**: [Join our Discord](https://discord.gg/SDDQ6hd9Rc)
- **Documentation**: [Wiki](https://github.com/PrivacyRights/NPT-GPU-Miner/wiki)

## 🙏 Acknowledgments

- **Neptune Cash Team** for the blockchain
- **CatsPool** for mining pool infrastructure
- **NVIDIA** for CUDA technology
- **Open Source Community** for contributions

<!-- ## 📊 Donations

If this miner helps you earn NPT, consider donating to support development:

- **NPT Address**: `[Your donation address]`
- **USDT BEP20**: `[Your BTC address]` -->

---

**🔗 Links**:
- [Neptune Cash Official Website](https://neptune.cash)
- [CatsPool Mining Pool](https://catspool.org)
- [NVIDIA CUDA Documentation](https://docs.nvidia.com/cuda/)
