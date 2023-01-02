NAME = philo
CC = gcc
CFLAGS = -g -Wall -Wextra -Werror
LIB = libft/libft.a
MAIN = src/main.c
SRCS = main.c \
		err.c

OBJS = *.o

all: $(NAME)

$(NAME): $(OBJS)
	@make -C libft
	$(CC) $(CFLAGS) $(OBJS) $(LIB) -o $(NAME)

$(OBJS): $(SRCS)
	$(CC) $(CFLAGS) -c $(SRCS)

clean:
	@make fclean -C libft
	rm -rf $(OBJS)
	rm -rf $(NAME)
	@clear

fclean: clean

re: fclean all
	@clear

git: clean
	git add .
	git commit
	git push