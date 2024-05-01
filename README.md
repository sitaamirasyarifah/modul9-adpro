Reflection

# Name : Sita Amira Syarifah
# NPM  : 2206023023
# Adpro C

1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?
Answer :
Unary RPC: In a unary RPC, the client sends a single request to the server and waits for a single response. It's suitable for simple, one-off requests where a single input corresponds to a single output without the need for streaming or ongoing interaction.
Server Streaming RPC: In server streaming RPC, the client sends a single request to the server, and the server responds with a stream of messages. This is suitable for scenarios where the server needs to send multiple responses to a single request, such as real-time data feeds or sending large amounts of data in chunks.
Bidirectional Streaming RPC: In bidirectional streaming RPC, both the client and the server can send a stream of messages independently. This is suitable for scenarios where there's a need for continuous communication between client and server, such as chat applications, real-time collaborative editing, or interactive gaming.

2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?
Answer :
When implementing a gRPC service in Rust, security considerations include authentication, authorization, and data encryption. This involves implementing authentication mechanisms such as OAuth or JWT for verifying the identity of clients, authorization mechanisms for determining what actions clients are allowed to perform, and data encryption using protocols like TLS to secure the communication channel between clients and servers.

3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?
Answer :
Potential challenges with bidirectional streaming in Rust gRPC include managing concurrent streams, handling errors and timeouts, ensuring message order and delivery, and dealing with backpressure to prevent overwhelming either the client or the server, especially in scenarios like chat applications where real-time communication is critical.

4. What are the advantages and disadvantages of using the tokio_stream::wrappers::ReceiverStream for streaming responses in Rust gRPC services?
Answer :
tokio_stream::wrappers::ReceiverStream: Using ReceiverStream provides a convenient way to convert a tokio::sync::mpsc::Receiver into a stream that can be used with gRPC services. Advantages include ease of use and compatibility with Tokio-based asynchronous programming. However, it may introduce overhead compared to more low-level stream implementations, and it may not be suitable for scenarios requiring fine-grained control over stream behavior.

5. In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?
Answer :
To facilitate code reuse and modularity in Rust gRPC services, you can organize your code into separate modules for different functionalities, define reusable traits for common behavior, use dependency injection for managing dependencies, and follow best practices for separation of concerns and single responsibility principle.

6. In the MyPaymentService implementation, what additional steps might be necessary to handle more complex payment processing logic?
Answer :
In the implementation of more complex payment processing logic in MyPaymentService, additional steps may include handling transactional consistency, error recovery, concurrency control, validation of payment requests, integration with external payment gateways or systems, and logging and monitoring for auditing and troubleshooting purposes.

7. What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?
Answer :
Adopting gRPC as a communication protocol can impact the overall architecture and design of distributed systems by providing a more efficient and standardized way to define and communicate service interfaces, enabling better performance, scalability, and maintainability. However, it may also introduce dependencies on gRPC-specific tooling and libraries and may require additional considerations for interoperability with other technologies and platforms.

8. What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?
Answer :
Compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs, HTTP/2 offers advantages such as improved performance through multiplexing, header compression, and server push, better support for streaming and real-time communication, and enhanced security features. However, it may introduce complexity in terms of implementation and debugging, and it may not be fully supported by all existing infrastructure and tooling.

9. How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?
Answer :
The request-response model of REST APIs contrasts with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness. REST APIs are based on synchronous request-response interactions, which may introduce latency and overhead, especially for long-running operations or real-time scenarios. In contrast, gRPC's bidirectional streaming allows for more efficient and responsive communication, enabling real-time updates and interactions between clients and servers.

10. What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?
Answer :
Using Protocol Buffers for defining service interfaces and message formats in gRPC offers advantages such as stronger type safety, more efficient serialization and deserialization, and automatic code generation for multiple programming languages. However, it may also introduce constraints in terms of schema evolution and compatibility, as changes to the schema may require coordination between clients and servers, and it may not be as flexible as JSON in terms of handling dynamic or unstructured data.
