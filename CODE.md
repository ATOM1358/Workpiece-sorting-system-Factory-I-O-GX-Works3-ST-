M0 := (X1 OR M0) AND NOT X0;

IF M0 THEN
    DMOV(TRUE, 16#1FFFFFFF, K8Y0);
    Y53 := TRUE;
    Y54 := TRUE;
    Y55 := TRUE;
    Y20 := TRUE;
    Y21 := TRUE;
    Y22 := TRUE;
    Y23 := TRUE;
    Y24 := TRUE;
    Y25 := TRUE;
    Y26 := TRUE;
    Y27 := TRUE;
    Y28 := TRUE;
	ELSE
    DMOV(TRUE, 16#0, K8Y0);
    Y53 := FALSE;
    Y54 := FALSE;
    Y55 := FALSE;
    Y20 := FALSE;
    Y21 := FALSE;
    Y22 := FALSE;
    Y23 := FALSE;
    Y24 := FALSE;
    Y25 := FALSE;
    Y26 := FALSE;
    Y27 := FALSE;
    Y28 := FALSE;
END_IF;

IF X2 AND M0 THEN
    Y29 := TRUE;
END_IF;
OUT_T(Y29, T30, 10);
IF T30 THEN
    Y29 := FALSE;
END_IF;

IF X3 AND M0 THEN
    Y30 := TRUE;
END_IF;
OUT_T(Y30, T31, 10);
IF T31 THEN
    Y30 := FALSE;
END_IF;

IF X4 AND M0 THEN
    Y31 := TRUE;
END_IF;
OUT_T(Y31, T32, 10);
IF T32 THEN
    Y31 := FALSE;
END_IF;

IF X5 AND M0 THEN
    Y32 := TRUE;
END_IF;
OUT_T(Y32, T33, 10);
IF T33 THEN
    Y32 := FALSE;
END_IF;

IF X6 AND M0 THEN
    Y33 := TRUE;
END_IF;
OUT_T(Y33, T34, 10);
IF T34 THEN
    Y33 := FALSE;
END_IF;

IF X7 AND M0 THEN
    Y34 := TRUE;
END_IF;
OUT_T(Y34, T35, 10);
IF T35 THEN
    Y34 := FALSE;
END_IF;

Y35 := X8 AND M0;
Y37 := X10 AND M0;
Y39 := X12 AND M0;
Y41 := X13 AND M0;
Y42 := X11 AND M0;
Y43 := X9 AND M0;

Y36 := X16 AND M0;
Y38 := X17 AND M0;
Y40 := X18 AND M0;

OUT_T((D0 = 1), T0, 10);
OUT_T((D0 = 2), T1, 5);
OUT_T((D0 = 3), T2, 10);
OUT_T((D0 = 4), T3, 15);
OUT_T((D0 = 5), T4, 10);
OUT_T((D0 = 6), T5, 5);
OUT_T((D0 = 7), T6, 10);
OUT_T((D0 = 8), T7, 15);

CASE D0 OF
    0:
	IF Y35 AND Y43 AND X9 AND M0 THEN
		D0 := 1;
	END_IF;

    1:
	IF T0 THEN
		D0 := 2;
	END_IF;

    2:
	IF T1 THEN
		D0 := 3;
	END_IF;

    3:
	IF T2 THEN
		D0 := 4;
	END_IF;

    4:
	IF T3 THEN
		D0 := 5;
	END_IF;

    5:
	IF T4 THEN
		D0 := 6;
	END_IF;

    6:
	IF T5 THEN
		D0 := 7;
	END_IF;

    7:
	IF T6 THEN
		D0 := 8;
	END_IF;

    8:
	IF T7 THEN
		D0 := 0;
	END_IF;
END_CASE;

Y44 := (D0 >= 4 AND D0 <= 7);
Y45 := (D0 = 1) OR (D0 = 2) OR (D0 = 5) OR (D0 = 6);
Y46 := (D0 >= 2 AND D0 <= 5);

OUT_T((D10 = 1), T10, 10);
OUT_T((D10 = 2), T11, 5);
OUT_T((D10 = 3), T12, 10);
OUT_T((D10 = 4), T13, 15);
OUT_T((D10 = 5), T14, 10);
OUT_T((D10 = 6), T15, 5);
OUT_T((D10 = 7), T16, 10);
OUT_T((D10 = 8), T17, 15);

CASE D10 OF
    0:
	IF Y37 AND Y42 AND X11 AND M0 THEN
		D10 := 1;
	END_IF;

    1:
	IF T10 THEN
		D10 := 2;
	END_IF;

    2:
	IF T11 THEN
		D10 := 3;
	END_IF;

    3:
	IF T12 THEN
		D10 := 4;
	END_IF;

    4:
	IF T13 THEN
		D10 := 5;
	END_IF;

    5:
	IF T14 THEN
		D10 := 6;
	END_IF;

    6:
	IF T15 THEN
		D10 := 7;
	END_IF;

    7:
	IF T16 THEN
		D10 := 8;
	END_IF;

    8:
	IF T17 THEN
		D10 := 0;
	END_IF;
END_CASE;

Y47 := (D10 >= 4 AND D10 <= 7);
Y48 := (D10 = 1) OR (D10 = 2) OR (D10 = 5) OR (D10 = 6);
Y49 := (D10 >= 2 AND D10 <= 5);

OUT_T((D20 = 1), T20, 10);
OUT_T((D20 = 2), T21, 5);
OUT_T((D20 = 3), T22, 10);
OUT_T((D20 = 4), T23, 15);
OUT_T((D20 = 5), T24, 10);
OUT_T((D20 = 6), T25, 5);
OUT_T((D20 = 7), T26, 10);
OUT_T((D20 = 8), T27, 15);

CASE D20 OF
    0:
	IF Y39 AND Y41 AND X13 AND M0 THEN
		D20 := 1;
	END_IF;

    1:
	IF T20 THEN
		D20 := 2;
	END_IF;

    2:
	IF T21 THEN
		D20 := 3;
	END_IF;

    3:
	IF T22 THEN
		D20 := 4;
	END_IF;

    4:
	IF T23 THEN
		D20 := 5;
	END_IF;

    5:
	IF T24 THEN
		D20 := 6;
	END_IF;

    6:
	IF T25 THEN
		D20 := 7;
	END_IF;

    7:
	IF T26 THEN
		D20 := 8;
	END_IF;

    8:
	IF T27 THEN
		D20 := 0;
	END_IF;
END_CASE;

Y50 := (D20 >= 4 AND D20 <= 7);
Y51 := (D20 = 1) OR (D20 = 2) OR (D20 = 5) OR (D20 = 6);
Y52 := (D20 >= 2 AND D20 <= 5);

Y8 := (M0 AND NOT Y43) OR (Y36 AND X16);
Y7 := (M0 AND NOT Y42) OR (Y38 AND X17);
Y6 := (M0 AND NOT Y41) OR (Y40 AND X18);

IF Y43 AND NOT (Y36 AND X16) THEN
    Y8 := FALSE;
END_IF;

IF Y42 AND NOT (Y38 AND X17) THEN
    Y7 := FALSE;
END_IF;

IF Y41 AND NOT (Y40 AND X18) THEN
    Y6 := FALSE;
END_IF;

IF Y35 THEN
    Y19 := FALSE;
END_IF;

Y56 := NOT Y8 AND M0;
Y57 := NOT Y7 AND M0;
Y58 := NOT Y6 AND M0;

IF NOT M0 THEN
    D0 := 0;
    D10 := 0;
    D20 := 0;
    Y29 := FALSE;
    Y30 := FALSE;
    Y31 := FALSE;
    Y32 := FALSE;
    Y33 := FALSE;
    Y34 := FALSE;
    Y44 := FALSE;
    Y45 := FALSE;
    Y46 := FALSE;
    Y47 := FALSE;
    Y48 := FALSE;
    Y49 := FALSE;
    Y50 := FALSE;
    Y51 := FALSE;
    Y52 := FALSE;
    Y36 := FALSE;
    Y38 := FALSE;
    Y40 := FALSE;
    Y8 := FALSE;
    Y7 := FALSE;
    Y6 := FALSE;
    Y56 := FALSE;
    Y57 := FALSE;
    Y58 := FALSE;
END_IF;

Y27 := Y35 AND M0;
Y28 := Y37 AND M0;
Y59 := Y39 AND M0;
