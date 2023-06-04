sequenceDiagram
    participant Customer
    participant Sender
    participant SenderBank
    participant SFSPNetwork
    participant ReceiverBank
    participant Receiver
    participant RubleAccount
    participant CryptoExchange
    participant CryptoWallet
    participant DollarAccount

    Customer->>Sender: Initiate Payment
    Sender->>SenderBank: Send Payment Request
    SenderBank->>SFSPNetwork: Validate Payment Request
    SFSPNetwork->>ReceiverBank: Send Payment Request
    ReceiverBank->>Receiver: Notify Payment Received
    Receiver->>RubleAccount: Deposit Ruble
    RubleAccount->>CryptoExchange: Exchange Ruble to Crypto
    CryptoExchange->>CryptoWallet: Transfer Crypto
    CryptoWallet->>DollarAccount: Exchange Crypto to Dollar
    DollarAccount->>SenderBank: Payment Confirmation
    SenderBank->>Sender: Transfer Payment
