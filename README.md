# Generar el template
1. Instalar cargo-generate: `cargo install cargo-generate`
2. Ejecutarlo, apuntando a gortegasntt/flex-gateway-policy-template: `cargo generate gortegasntt/flex-gateway-policy-template`
3. Introducir el nombre, sustituyendo los espacios por guiones
4. Si es necesario, modificar el nombre para quitar los guiones en definition, schema e implementation

# Compilar política

Hay dos opciones:
- `cargo build --target wasm32-wasi --release`
- `cargo build --target wasm32-unknown-unknown --release`

La diferencia entre estas dos formas de compilar es la siguiente:
>WASI is an extended WASM environment specification, which tries to emulate a full OS, including system calls and functionality related to file system, networking, and so forth. In contrast, wasm32-unknown-unknown is a bare metal-like target (hence the unknowns in the target triple — those would specify the OS), which doesn't provide much functionality outside of pure computation.