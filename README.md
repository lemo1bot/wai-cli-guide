# w.ai CLI Guide - Earn W Points with Your Internet & GPU

Hey crypto fam! 👋 

Just discovered this cool way to earn W points by running w.ai nodes. Basically, you rent out your internet connection and GPU power to help their AI network. Pretty sweet passive income setup!

## Need Help? Join Our Community! 🤝

If you run into issues or want to connect with other w.ai miners:

- **Follow me on Twitter**: [@bank_of_btc](https://x.com/bank_of_btc) for updates and tips
- **Join our Telegram group**: [Rosla](https://t.me/rooslaa) for step-by-step guides and crypto insights
- **Stay updated** with the latest w.ai strategies and community tips

---

## What You Can Earn 🤑

- **W Points**: Earn points for every task your node completes
- **Future Rewards**: Points likely convert to tokens later
- **Passive Income**: Run 24/7, earn while you sleep
- **Scalable**: More nodes = more earnings

## What You Need (The Basics)

### Hardware Requirements:
- **Mac**: Any M-series chip (M1, M2, M3, M4)
- **Windows/Linux**: NVIDIA GPU (GTX 1050+ or RTX series)
- **RAM**: 8GB minimum (16GB+ recommended)
- **Storage**: 50GB+ free space

### Internet Requirements:
- **Speed**: 10+ Mbps download, 5+ Mbps upload
- **Stability**: No frequent disconnections
- **Unlimited**: No data caps (you'll use a lot)
- **Latency**: Lower is better for faster rewards

## Quick Start (5 Minutes Setup)

### Step 1: Get Your API Key
1. Go to [w.ai dashboard](https://w.ai/r/V3XBMXWW)
2. Sign up with email
3. Go to "API Keys" section
4. Create new key
5. Copy it - you'll need this!

### Step 2: Install w.ai CLI
```bash
# One-liner install
curl -fsSL https://app.w.ai/install.sh | bash

# Check if it worked
wai --version
```

### Step 3: Start Mining
```bash
# Set your API key
export W_AI_API_KEY=your_api_key_here

# Start your first node
wai run
```

That's it! You're now earning W points! 🎉

## Advanced Setup (Multiple Nodes)

### Install PM2 for Multi-Node Management
```bash
# Install PM2
npm install -g pm2

# Create config file
cat > wai.config.js << 'CONFIG'
module.exports = {
  apps : [{
    name: 'wai-miner',
    script: 'wai',
    args: 'run',
    instances: 4,  // Number of nodes
    autorestart: true,
    watch: false,
    max_memory_restart: '1G',
    env: {
      NODE_ENV: 'production',
      W_AI_API_KEY: 'your-api-key-here'
    }
  }]
};
CONFIG

# Start multiple nodes
pm2 start wai.config.js
```

### Monitor Your Earnings
```bash
# Check all nodes
pm2 list

# View logs
pm2 logs wai-miner

# Monitor GPU usage
nvidia-smi

# Check internet usage
iftop
```

## Internet Optimization Tips 🌐

### Best Practices:
- **Wired Connection**: Ethernet > WiFi for stability
- **Router Setup**: Port forwarding if needed
- **Bandwidth**: Dedicate 50+ Mbps for mining
- **Backup**: Consider mobile hotspot as backup

### Troubleshooting:
```bash
# Test your connection
speedtest-cli

# Check latency
ping 8.8.8.8

# Monitor bandwidth
nethogs
```

## Earnings Strategy 💰

### What Affects Earnings:
- **Node Uptime**: 24/7 = max earnings
- **Internet Speed**: Faster = more tasks
- **GPU Power**: Better GPU = higher rewards
- **Location**: Some regions get more tasks

### Scaling Tips:
- Start with 1 node, monitor for 24 hours
- Add nodes gradually (2, 4, 8, etc.)
- Monitor your internet usage
- Keep track of earnings in dashboard

## Cool Features I Discovered 🚀

### Auto-Restart on Crash
```bash
# PM2 keeps your nodes running
pm2 startup
pm2 save
```

### Remote Monitoring
```bash
# Check nodes from anywhere
pm2 monit

# Get status via API
pm2 jlist
```

### Performance Optimization
```bash
# GPU monitoring
watch -n 1 nvidia-smi

# Memory usage
htop

# Network monitoring
iftop -i eth0
```

## My Experience & Tips

### What Worked for Me:
- **Started with 1 node**: Tested for 24 hours
- **Scaled to 4 nodes**: My internet could handle it
- **Used PM2**: Keeps everything running smoothly
- **Monitored closely**: Tracked earnings daily

### Common Issues & Fixes:
1. **"Connection timeout"**: Check your internet stability
2. **"GPU memory full"**: Reduce number of nodes
3. **"API key invalid"**: Double-check your key
4. **"No tasks available"**: Wait, they come in waves

### Pro Tips:
- **Run 24/7**: Maximum uptime = maximum earnings
- **Monitor costs**: Track electricity + internet usage
- **Join community**: Stay updated on new features
- **Backup setup**: Have a second machine ready

## Earnings Dashboard 📊

Check your progress at [w.ai dashboard](https://w.ai/r/V3XBMXWW):
- **W Points earned**: Real-time tracking
- **Node status**: Uptime and performance
- **Task history**: What your nodes completed
- **Leaderboard**: Compare with other miners

## Future Potential 🌟

- **Token Launch**: W points might convert to tokens
- **Staking**: Future staking opportunities
- **Governance**: Points might give voting rights
- **Partnerships**: More earning opportunities

## Where to Get Help

- **Official w.ai Documentation**: https://docs.w.ai/w.ai-guide/supported-hardware
- **w.ai Dashboard**: https://w.ai/r/V3XBMXWW
- **Community Support**: Join our Telegram group!

---

**Guide created by**: [@bank_of_btc](https://x.com/bank_of_btc)

**Based on**: My actual mining experience with w.ai

**When I tested**: August 2025

---

*This is my experience mining W points with w.ai. Your earnings may vary, but this should get you started on the path to passive income!*

#wai #Mining #PassiveIncome #GPU #AI
