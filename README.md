# check4

PROCEDURE sort(VAR arr : ARRAY_OF INTEGER)
VAR
    i,j,hand : INTEGER;
BEGIN
    FOR i FROM 1 TO arr.length-1 DO
        hand := arr [i];
        j := i-1;
        WHILE (j >= 0 AND arr[j] > hand) DO
            arr[j+1] := arr[j];
            j := j-1;
        END_WHILE
        arr[j+1] = hand;
    END_FOR
END
