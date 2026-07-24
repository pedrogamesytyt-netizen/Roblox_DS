# =============================================================================
# Makefile Padrão para PS2SDK (C / C++)
# =============================================================================

# Nome do arquivo de saída (.elf) que será gerado
EE_BIN = openblox_ps2.elf

# Lista de arquivos de código fonte (.cpp e .c) que devem ser compilados.
# Adicione aqui os objetos correspondentes aos seus arquivos em source/
EE_OBJS = source/main.o

# Pastas de inclusão de cabeçalhos (.h / .hpp)
EE_INCS = -I$(PS2SDK)/ee/include -I$(PS2SDK)/ports/include -Iinclude

# Bibliotecas de vinculação (Linker)
# Como o projeto usa C++, adicionamos -lstdc++ e as libs básicas de tela/controle do PS2
EE_LIBS = -lgraph -ldraw -lpad -lkernel -lps2sdk -lstdc++ -lm

# Flags de compilação (O2 para otimização de desempenho)
EE_CFLAGS = -O2 -Wall
EE_CXXFLAGS = -O2 -Wall -fno-rtti -fno-exceptions

# =============================================================================
# Regras do PS2SDK (Não altere estas linhas abaixo)
# =============================================================================
ifeq ($(strip $(PS2SDK)),)
$(error "A variável PS2SDK não está definida no ambiente.")
endif

include $(PS2SDK)/samples/Makefile.pref
include $(PS2SDK)/samples/Makefile.eerules
