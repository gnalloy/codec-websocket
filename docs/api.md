# API Reference

[简体中文](api.zh-CN.md) | [Docs Index](README.md)

This inventory is generated from `go doc -short` for the packages in this repository. It is a quick public-surface map; source files and tests remain the authority for exact semantics.

## Packages

### `gnalloy.org/codec-websocket`

Package name: `websocket`

```text
const OpcodeContinuation = 0x0 ...
const CloseStatusNormalClosure uint16 = 1000 ...
var ErrInvalidHandshake = errors.New("gnalloy/codec/websocket: invalid websocket handshake") ...
func AcceptKey(key string) string
func IsUpgradeRequest(req http1.Request) bool
func IsValidCloseStatusCode(code uint16) bool
type ClientHandshakeConfig struct{ ... }
type ClientHandshakeHandler struct{ ... }
    func NewClientHandshakeHandler(config ClientHandshakeConfig) (*ClientHandshakeHandler, error)
type CloseState uint8
    const CloseStateOpen CloseState = iota ...
type CloseStateEvent struct{ ... }
type CloseStatus struct{ ... }
    func ParseCloseStatus(frame Frame) (CloseStatus, bool)
type ControlFrameHandler struct{ ... }
    func NewControlFrameHandler() *ControlFrameHandler
type FragmentAggregator struct{ ... }
    func NewFragmentAggregator(maxMessageLength int) *FragmentAggregator
type Frame struct{ ... }
    func NewCloseFrame(ctx *channel.HandlerContext, code uint16, reason string) (Frame, error)
type FrameDecoder struct{ ... }
    func NewClientFrameDecoder(maxFrameLength int) (*FrameDecoder, error)
    func NewFrameDecoder(maxFrameLength int) (*FrameDecoder, error)
    func NewFrameDecoderWithConfig(cfg FrameDecoderConfig) (*FrameDecoder, error)
    func NewFrameDecoderWithMaskPolicy(maxFrameLength int, expectMaskedFrames bool, allowMaskedFrames bool) (*FrameDecoder, error)
    func NewServerFrameDecoder(maxFrameLength int) (*FrameDecoder, error)
type FrameDecoderConfig struct{ ... }
type FrameEncoder struct{}
    func NewFrameEncoder() *FrameEncoder
type HandshakeComplete struct{ ... }
type IdleHandler struct{ ... }
    func NewIdleHandler(pingPayload []byte, closeCode uint16, closeReason string) *IdleHandler
type ServerHandshakeHandler struct{ ... }
    func NewServerHandshakeHandler(path string, removeHandlers ...string) *ServerHandshakeHandler
type UTF8Validator struct{ ... }
    func NewUTF8Validator() *UTF8Validator
```

### `gnalloy.org/codec-websocket/deflate`

Package name: `deflate`

```text
const FrameExtensionName = "deflate-frame" ...
const DefaultMaxMessageBytes = 32 << 20
const ExtensionName = "permessage-deflate"
var ErrInvalidConfig = errors.New("gnalloy/codec/websocket/deflate: invalid config") ...
func Offer(params Parameters) string
func OfferFrameExtension() string
func ParseFrameExtension(header string) (string, bool, error)
type Compressor struct{ ... }
    func NewCompressor(cfg Config) (*Compressor, error)
type Config struct{ ... }
type Decompressor struct{ ... }
    func NewDecompressor(cfg Config) (*Decompressor, error)
type LegacyFrameCompressor struct{ ... }
    func NewLegacyFrameCompressor(cfg Config) (*LegacyFrameCompressor, error)
type LegacyFrameDecompressor struct{ ... }
    func NewLegacyFrameDecompressor(cfg Config) (*LegacyFrameDecompressor, error)
type Parameters struct{ ... }
    func Parse(header string) (Parameters, bool, error)
```
