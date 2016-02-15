## Using bit field to achieve compact representation.

    struct Date {
    	unsigned short day_of_week: 3;  // [1, 7]
    	unsigned short day_of_month: 5; // [1, 31]
    	unsigned short month: 4;        // [1, 12]
    	unsigned short year: 16;         // [0, 131071]
    	unsigned short bc_or_ad: 1;     // [0, 1]
    };

NOTE: `GCC` and `MSVC` have different strategies to pack bits. While GCC would try to pack bits consecutively, MSVC would decide whether the next field would fully fit into the current slot or not. If not, it would start a new slot for the next field. For the above example, `MSVC` would take 3 unsigned short instead of 2. If moving `bc_or_ad` above `year`, `MSVC` would take 2 unsigned short, as expected.