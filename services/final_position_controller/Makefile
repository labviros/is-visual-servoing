COMPILER = g++
FLAGS = -std=c++14 -O3 -Wall -Werror -Wextra

SO_DEPS = $(shell pkg-config --libs --cflags libSimpleAmqpClient msgpack librabbitmq)
SO_DEPS += -lboost_program_options -lpthread -larmadillo

all: final_position_controller

clean:
	rm final_position_controller
	
final_position_controller: final_position_controller.cpp 
	$(COMPILER) $^ -o $@ $(FLAGS) $(SO_DEPS)