# qb-mechanic
esx_mechanic converted to QBCore, nice visual and works 100%


# HOW TO INSTALL

EN:
Basic installation just make sure to add in server.cfg

"start qb-mechanic"

ES:
Instalación básica, solo asegurate de añadir esto en tu server.cfg

"start qb-mechanic"


Also, if using qb-core, make sure to add those functions in qb-core/client/functions.lua

||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||

QBCore.Functions.MathRound = function(value, numDecimalPlaces)
    if numDecimalPlaces then
        local power = 10^numDecimalPlaces
        return math.floor((value * power) + 0.5) / (power)
    else
        return math.floor(value + 0.5)
    end
end

QBCore.Functions.MathGroupDigits = function(value)
    local left,num,right = string.match(value,'^([^%d]*%d)(%d*)(.-)$')

    return left..(num:reverse():gsub('(%d%d%d)','%1' .. _U('locale_digit_grouping_symbol')):reverse())..right
end

QBCore.Functions.MathTrim = function(value)
    if value then
        return (string.gsub(value, "^%s*(.-)%s*$", "%1"))
    else
        return nil
    end
end

||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
