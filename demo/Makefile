FILES = $(addprefix test-non-interactive-, 1 2 3) $(addprefix test-interactive-, 4 5 6)

all: $(FILES)

test-non-interactive-%:
	./get-shared-terminal-demo "$*" > "$@" || { rm -f "$@"; false; }

test-interactive-%:
	./get-shared-terminal-demo "$*" -i > "$@" || { rm -f "$@"; false; }

clean:
	rm -f $(FILES)
