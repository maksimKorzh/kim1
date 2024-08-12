================================
 6502 Chess by Code Monkey King
================================
 ORIGINS:
  0x0000 Board and variables
  0x0100 Evaluation
  0x0200 Search

 Enter moves by directly changing board in memory:

  00  16 14 15 17 13 15 14 16    Coordinates layout: RANK+FILE e.g. 64 = E2 
  10  12 12 12 12 12 12 12 12
  20  00 00 00 00 00 00 00 00    $09 - White pawn      $12 - Black pawn
  30  00 00 00 00 00 00 00 00    $0C - White knight    $14 - Black knight
  40  00 00 00 00 00 00 00 00    $0D - White bishop    $15 - Black bishop
  50  00 00 00 00 00 00 00 00    $0E - White rook      $16 - Black rook
  60  09 09 09 09 09 09 09 09    $0F - White queen     $17 - Black queen
  70  0E 0C 0D 0F 0B 0D 0C 0E    $0B - White king      $13 - Black king
      
      00 01 02 03 04 05 06 07    $00BC - Side to move, $08: white, $10: black

If you want engine to male move for the current side to move do:
  0200 [SPACE] [G] - engine would search the move, make it and print the board

If you want to check board position after you have made the move do:
  03F6 [SPACE] [G] - this would print current board state and side to move
