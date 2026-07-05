/* New Things Every Day — Da 107 */
/* Groups items by category and counts them */

function dailyLog107() {
    const items = [
        { name: "Keyboard", category: "Hardware" },
        { name: "Mouse", category: "Hardware" },
        { name: "Node.js", category: "Software" },
        { name: "Git", category: "Software" },
        { name: "Notebook", category: "Office" }
    ];

    const summary = items.reduce((result, item) => {
        result[item.category] = (result[item.category] || 0) + 1;
        return result;
    }, {});

    console.log({
        day: 107,
        timestamp: new Date().toISOString(),
        categories: summary,
        totalItems: items.length
    });
}

dailyLog107();
