CC = gcc
CFWK_DIR = ..
target =  test

C_FLAGS=
src=  $(CFWK_DIR)/cf_test/cf_test.c \
	  $(CFWK_DIR)/cf_allocator/cf_allocator_simple.c \
	  $(CFWK_DIR)/cf_collection/cf_list.c \
	  $(CFWK_DIR)/cf_collection/cf_hash.c \
	  $(CFWK_DIR)/cf_collection/cf_string.c \
	  $(CFWK_DIR)/cf_collection/cf_iterator.c \
	  $(CFWK_DIR)/cf_module/cf_module.c \
	  $(CFWK_DIR)/cf_factory/cf_factory.c \
	  $(CFWK_DIR)/cf_factory/cf_element.c \
	  $(CFWK_DIR)/cf_factory/cf_pad.c \
	  $(CFWK_DIR)/cf_factory/cf_element_class.c \
	  $(CFWK_DIR)/cf_http/cf_http_parser.c \
	  $(CFWK_DIR)/cf_net/cf_socket.c \
	  $(CFWK_DIR)/cf_net/cf_socket_linux.c \
	  $(CFWK_DIR)/cf_websocket/cf_websocket_server.c \
	  $(CFWK_DIR)/cf_test_case/cf_list_test.c \
	  $(CFWK_DIR)/cf_test_case/cf_module_test.c \
	  $(CFWK_DIR)/cf_test_case/cf_factory_test.c \
	  $(CFWK_DIR)/cf_test_case/cf_websocket_test.c \
	  $(CFWK_DIR)/cf_test_case/cf_test_top.c

obj := $(src:c=o)

all:	$(obj)
	$(CC)	-g $(C_FLAGS) -I$(CFWK_DIR) $^ -o $(target)
$(obj): %.o : %.c
	$(CC) -g $(C_FLAGS) -I$(CFWK_DIR) -o $@ -c $^
clean:
	rm $(obj) $(target)
