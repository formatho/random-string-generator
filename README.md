# Random String Generator - Privacy-First Developer Tool

[![Stars](https://img.shields.io/github/stars/formatho/random-string-generator?style=social)](https://github.com/formatho/random-string-generator)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Privacy First](https://img.shields.io/badge/Privacy-First%20%F0%9F%94%92-success)](https://formatho.com)
[![Try Online](https://img.shields.io/badge/Try%20Online-Online%20%F0%9F%8C%90-blue)](https://formatho.com/tools)

A fast, secure, and privacy-first random string generator that creates random strings entirely in your browser. No data is ever sent to a server, ensuring complete privacy and security for your generated strings.

## 🚀 Features

- **Instant Generation**: Generate random strings instantly
- **Privacy-First**: All processing happens client-side in your browser
- **No Tracking**: Zero analytics, zero cookies, zero data collection
- **Multiple Formats**: Alphanumeric, alphabetic, numeric, hexadecimal, binary
- **Custom Length**: Generate strings from 1 to 10,000 characters
- **Batch Generation**: Generate multiple strings at once
- **Exclude Characters**: Exclude specific characters from generation
- **Cryptographically Secure**: Uses Web Crypto API for secure randomness
- **One-Click Copy**: Copy generated strings to clipboard instantly
- **History Tracking**: Keep track of generated strings
- **Pattern Support**: Generate strings with custom patterns

## 📖 Why Privacy Matters

Traditional random string generators send your data to remote servers, exposing sensitive information:

- Passwords and authentication tokens
- API keys and secret tokens
- Session identifiers and tokens
- Temporary passwords and reset codes
- Encryption keys and salts
- Unique identifiers and tokens
- One-time passwords (OTPs)
- Cryptographic nonces

**Formatho processes everything in your browser** - your generated strings never leave your device.

## 🔧 How It Works

### Random String Generation

Random string generation uses cryptographically secure random number generation to create unpredictable strings.

**Alphanumeric:**
```
aB3xY9zQ2pL7
```

**Alphabetic:**
```
KjHmNpQrStUv
```

**Numeric:**
```
8472910347
```

**Hexadecimal:**
```
3a7f9c2e5d1b4f6a8c0e2d4
```

**Binary:**
```
110101001010011010010101
```

### Cryptographic Security

Uses Web Crypto API (`crypto.getRandomValues()`) for cryptographically secure random number generation:

- Unpredictable: Cannot be predicted by attackers
- Uniform distribution: Each character has equal probability
- Secure: Suitable for security-sensitive applications

### Custom Patterns

Generate strings with custom patterns:

**Example Pattern:**
```
XXXX-XXXX-XXXX-XXXX
```

**Result:**
```
aB3x-Y9zQ-2pL7-kJhM
```

## 💻 Usage

### Web App

Visit [formatho.com/tools](https://formatho.com/tools) and:

1. **Select Format**: Choose string format (alphanumeric, alphabetic, etc.)
2. **Set Length**: Set string length (1-10,000 characters)
3. **Generate**: Click generate button to create string
4. **Batch**: Generate multiple strings at once
5. **Exclude**: Exclude specific characters
6. **Copy**: Click copy button to copy generated string
7. **History**: View and reuse generated strings

### NPM Package

```bash
npm install @formatho/random-string-generator
```

```javascript
import {
  generateRandomString,
  generatePassword,
  generateUUID,
  generateHex,
  generateBinary,
  generateFromPattern
} from '@formatho/random-string-generator';

// Generate random alphanumeric string
const alphanumeric = generateRandomString(16, 'alphanumeric');
console.log(alphanumeric);
// 'aB3xY9zQ2pL7kJhM'

// Generate password with requirements
const password = generatePassword({
  length: 16,
  uppercase: true,
  lowercase: true,
  numbers: true,
  symbols: true
});
console.log(password);
// 'Kj9#mN$pQ2@rS7!'

// Generate UUID v4
const uuid = generateUUID();
console.log(uuid);
// '9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'

// Generate hexadecimal string
const hex = generateHex(32);
console.log(hex);
// '3a7f9c2e5d1b4f6a8c0e2d4f6a8b9c0d'

// Generate binary string
const binary = generateBinary(24);
console.log(binary);
// '110101001010011010010101'

// Generate from pattern
const pattern = generateFromPattern('XXXX-XXXX-XXXX-XXXX', {
  uppercase: true,
  numbers: true
});
console.log(pattern);
// 'KJ9M-NPQ2-RS7!-X4Z9'
```

### Command Line

```bash
# Generate random string
npx @formatho/random-string-generator generate --length 16 --format alphanumeric

# Generate password
npx @formatho/random-string-generator password --length 16 --uppercase --numbers --symbols

# Generate UUID
npx @formatho/random-string-generator uuid

# Generate hex string
npx @formatho/random-string-generator hex --length 32

# Generate binary string
npx @formatho/random-string-generator binary --length 24

# Generate from pattern
npx @formatho/random-string-generator pattern "XXXX-XXXX-XXXX-XXXX" --uppercase --numbers
```

### Browser API

```javascript
import { generateRandomStringAsync } from '@formatho/random-string-generator/browser';

// Generate random string asynchronously (uses Web Crypto API)
const random = await generateRandomStringAsync(16, 'alphanumeric');
console.log(random);
// 'aB3xY9zQ2pL7kJhM'
```

## 🎯 Use Cases

- **Password Generation**: Generate strong, secure passwords
- **API Keys**: Generate API keys and tokens
- **Session Tokens**: Generate session identifiers
- **One-Time Passwords**: Generate OTPs and reset codes
- **Encryption**: Generate encryption keys and salts
- **Unique Identifiers**: Generate unique IDs and tokens
- **Testing**: Generate test data for applications
- **Privacy**: Safely generate strings without exposing them

## 🔒 Privacy & Security

At Formatho, we believe in privacy-first development:

- **Client-Side Processing**: All generation happens in your browser
- **No Server Communication**: Your generated strings never leave your device
- **No Analytics**: We don't track how you use this tool
- **No Cookies**: We don't store or use cookies
- **Open Source**: Code is available for security audits
- **MIT License**: Free to use, modify, and distribute

### ✅ Security Best Practices

**Cryptographically Secure:**
- ✅ Uses Web Crypto API (`crypto.getRandomValues()`)
- ✅ Suitable for security-sensitive applications
- ✅ Unpredictable and uniform distribution
- ✅ Resistant to statistical attacks

**Password Generation:**
- ✅ Mix of character types (uppercase, lowercase, numbers, symbols)
- ✅ Minimum length of 12 characters recommended
- ✅ Avoid common patterns and dictionary words
- ✅ Use unique passwords for each service

**NOT Suitable For:**
- ❌ Generate passwords with predictable patterns
- ❌ Use `Math.random()` for security-sensitive applications
- ❌ Use short strings for cryptographic keys
- ❌ Store passwords in plaintext

## 📊 Performance

| Operation | Time | Throughput |
|-----------|------|------------|
| Generate 16-char string | < 1ms | 16M chars/s |
| Generate 100-char string | < 2ms | 50M chars/s |
| Generate 1K-char string | < 10ms | 100M chars/s |
| Generate 100 strings (16 chars each) | < 50ms | 32 strings/ms |

*Benchmarks run on modern browsers (Chrome 120+, Firefox 120+, Safari 17+)*

## 🛠️ Installation

### For Web App

No installation required! Visit [formatho.com/tools](https://formatho.com/tools).

### For NPM Package

```bash
npm install @formatho/random-string-generator
```

### For Command Line

```bash
npm install -g @formatho/random-string-generator
```

## 📚 API Reference

### `generateRandomString(length: number, format: string): string`

Generates random string.

**Parameters:**
- `length` - String length (1-10,000)
- `format` - String format: 'alphanumeric', 'alphabetic', 'numeric', 'hexadecimal', 'binary'

**Returns:**
- Random string

**Example:**
```javascript
const random = generateRandomString(16, 'alphanumeric');
// Returns: 'aB3xY9zQ2pL7kJhM'
```

### `generatePassword(options?: PasswordOptions): string`

Generates random password.

**Parameters:**
- `options` - Optional configuration object
  - `length` - Password length (default: 16)
  - `uppercase` - Include uppercase letters (default: true)
  - `lowercase` - Include lowercase letters (default: true)
  - `numbers` - Include numbers (default: true)
  - `symbols` - Include symbols (default: true)

**Returns:**
- Random password

**Example:**
```javascript
const password = generatePassword({
  length: 16,
  uppercase: true,
  numbers: true,
  symbols: true
});
// Returns: 'Kj9#mN$pQ2@rS7!'
```

### `generateUUID(): string`

Generates UUID v4.

**Returns:**
- UUID v4 string

**Example:**
```javascript
const uuid = generateUUID();
// Returns: '9b1deb4d-3b7d-4bad-9bdd-2b0d7b3dcb6d'
```

### `generateHex(length: number): string`

Generates hexadecimal string.

**Parameters:**
- `length` - String length

**Returns:**
- Hexadecimal string

**Example:**
```javascript
const hex = generateHex(32);
// Returns: '3a7f9c2e5d1b4f6a8c0e2d4f6a8b9c0d'
```

### `generateBinary(length: number): string`

Generates binary string.

**Parameters:**
- `length` - String length

**Returns:**
- Binary string

**Example:**
```javascript
const binary = generateBinary(24);
// Returns: '110101001010011010010101'
```

### `generateFromPattern(pattern: string, options?: PatternOptions): string`

Generates string from pattern.

**Parameters:**
- `pattern` - Pattern string (X = alphanumeric, # = numeric, A = uppercase, a = lowercase)
- `options` - Optional configuration object

**Returns:**
- Generated string

**Example:**
```javascript
const pattern = generateFromPattern('XXXX-XXXX-XXXX-XXXX', {
  uppercase: true,
  numbers: true
});
// Returns: 'KJ9M-NPQ2-RS7!-X4Z9'
```

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md) for details.

## 🔗 Related Tools

- [UUID Generator](https://github.com/formatho/uuid-generator) - Generate UUIDs
- [Hash Generator](https://github.com/formatho/hash-generator) - Generate hash strings
- [Password Generator](https://formatho.com/tools/password-generator) - Generate secure passwords
- [Security Tools](https://formatho.com/tools) - More security tools

## 💬 Support

- **Issues**: [GitHub Issues](https://github.com/formatho/random-string-generator/issues)
- **Discussions**: [GitHub Discussions](https://github.com/formatho/random-string-generator/discussions)
- **Email**: support@formatho.com

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=formatho/random-string-generator&type=Date)](https://star-history.com/#formatho/random-string-generator&Date)

---

**Made with 🔒 by Formatho**

Privacy-first developer tools, 100+ utilities with zero tracking.

[Try Online](https://formatho.com/tools) | [More Tools](https://formatho.com) | [Privacy Policy](https://formatho.com/privacy)
## ⚡ Free API — Cloudflare Worker

This tool is also available as a free, zero-tracking API deployed on Cloudflare Workers:

**Endpoint:** https://random-string-formatho.filesformatho.workers.dev

Deploy it yourself: the complete Worker source is in [`worker/`](./worker) — `cd worker && wrangler deploy`. MIT licensed.

## 🔗 Links

- [Online tool](https://formatho.com/tools)
- [Live API](https://random-string-formatho.filesformatho.workers.dev)
