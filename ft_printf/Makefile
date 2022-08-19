# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: mdo-carm <mdo-carm@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/01/30 14:02:54 by mdo-carm          #+#    #+#              #
#    Updated: 2022/03/15 18:27:28 by mdo-carm         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libftprintf.a

C_SOURCE = ft_printf.c       \
           ft_printf_flags.c \

H_SOURCE = ft_printf.h

CC = gcc

C_FLAGS = -Wall   \
         -Wextra  \
         -Werror  \

OBJ = $(C_SOURCE:.c=.o)

all: $(NAME)

$(NAME): $(OBJ) $(H_SOURCE)
		ar -rcs $(NAME) $(OBJ)

%.o: %.c $(H_SOURCE)
		$(CC) $(C_FLAGS) -c $< -o $@

clean: 
		rm -rf $(OBJ)
		@echo "Libft cleaned"

fclean:	clean
		rm -rf $(NAME)
		@echo "Libft full cleaned"

re: fclean all

.PHONY: all clean fclean re