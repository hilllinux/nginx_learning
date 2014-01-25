CXX = gcc
CXXFLAGS += -g -Wall -Wextra
  
NGX_ROOT = /Users/wsq/workspace/nginx
  
TARGETS = ngx_basic_type
TARGETS_C_FILE = $(TARGETS).c
CORE_INCS = -I. \
    -I$(NGX_ROOT)/src/core \
    -I$(NGX_ROOT)/src/event \
    -I$(NGX_ROOT)/src/event/modules \
    -I$(NGX_ROOT)/src/os/unix \
    -I$(NGX_ROOT)/objs \
  
CLEANUP = rm -f $(TARGETS) *.o
all: $(TARGETS)

clean:
	$(CLEANUP)
$(TARGETS): $(TARGETS_C_FILE)
	$(CXX) $(CXXFLAGS) $(CORE_INCS) $^ -o $@

