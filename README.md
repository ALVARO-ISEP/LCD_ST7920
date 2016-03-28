# LCD_ST7920

KeyWords: AVR,ST7920,LCD128x64

Hello, I have searched for a avr-library for this LCD controller for a long time and have only find 3 types of libraries: 

  - A lot heavy but with a lot of functions and fonts

  - Parallel but about 10 pins wasted

  - too simple only been able to use lcd internal fonts that only allow 4 lines of text



So I have tried to make a library myself and this is the result. This is my first try on publish something so I am sorry if something is wrong but feel free to comment.


#Functions

##void lcd_init();

Initialize the lcd on pins 2(clock) ,3(data) and 4(reset) of the PORTC.

You can change the pins by changing the defines in the .h.


##void lcd_clear_all(void);

Clear the LCD display


##void lcd_draw(uint8_t *p);

Draw an 128x64 B/W picture in the LCD.

Image can be created with GIMP.


##void lcd_send_str8(line,columm, string[16]);

Write a string in the display, 8px height, in the line[0,7] and columm[0,7] specified.


##void lcd_set_cursor(int8_t line, int8_t col);

Set the cursor to the specified position. Line[0,3], columm[0,7].


##void lcd_send_str(char *str);

Used together with the previous function to write a string in the display, 16px height, wherever the cursor is.
